<script lang="js">
	import { onMount } from 'svelte';
	import createGlobe from 'cobe';
	import { spring } from 'svelte/motion';
	import { cn } from '$lib/utils';

	let x = spring(0, {
		stiffness: 0.04,
		damping: 0.4,
		precision: 0.005
	});

	let className = '';
	export { className as class };

	let pointerInteracting = null;
	let pointerInteractionMovement = 0;
	let canvas;
	let phi = 0;
	let width = 0;

	let onResize = () => {
		width = canvas.offsetWidth;
	};

	let onRender = (state) => {
		if (!pointerInteracting) {
			phi += 0.005;
		}
		state.phi = phi + $x;
		state.width = width * 2;
		state.height = width * 2;
	};

	onMount(() => {
		// Adds the resize event listener when the component is mounted
		window.addEventListener('resize', onResize);
		onResize();

		// Initializes the globe with specific options
		const globe = createGlobe(canvas, {
			devicePixelRatio: 2,
			width: width,
			height: width,
			phi: 0,
			theta: 0.3,
			dark: 1,
			diffuse: 0.6, // Increased for better light diffusion
			mapSamples: 16000,
			mapBrightness: 4.8, // Increased for more visible landmass
			baseColor: [0.1, 0.1, 0.3], // More blue-indigo base
			markerColor: [149 / 255, 97 / 255, 226 / 255], // Purple marker color
			glowColor: [120 / 255, 58 / 255, 183 / 255], // Indigo-purple glow
			markers: [
				{ location: [14.5995, 120.9842], size: 0.03 },
				{ location: [19.076, 72.8777], size: 0.03 },
				{ location: [23.8103, 90.4125], size: 0.05 },
				{ location: [30.0444, 31.2357], size: 0.07 },
				{ location: [39.9042, 116.4074], size: 0.08 },
				{ location: [-23.5505, -46.6333], size: 0.05 },
				{ location: [19.4326, -99.1332], size: 0.04 },
				{ location: [40.7128, -74.006], size: 0.1 },
				{ location: [34.6937, 135.5022], size: 0.05 },
				{ location: [41.0082, 28.9784], size: 0.06 }
			],
			onRender: onRender
		});

		// Removes the resize event listener when the component is unmounted to prevent memory leaks
		return () => {
			window.removeEventListener('resize', onResize);
		};
	});
</script>

<main class={cn('relative mx-auto aspect-[1/1] w-full max-w-[600px]', className)}>
	<div
		class="absolute inset-0 rounded-full bg-gradient-to-br from-indigo-900/30 to-purple-900/30 backdrop-blur-sm"
	></div>
	<canvas
		class="h-full w-full [contain:layout_paint_size]"
		bind:this={canvas}
		on:pointerdown={(e) => {
			pointerInteracting = e.clientX - pointerInteractionMovement;
			canvas.style.cursor = 'grabbing';
		}}
		on:pointerup={() => {
			pointerInteracting = null;
			canvas.style.cursor = 'grab';
		}}
		on:pointerout={() => {
			pointerInteracting = null;
			canvas.style.cursor = 'grab';
		}}
		on:mousemove={(e) => {
			if (pointerInteracting !== null) {
				const delta = e.clientX - pointerInteracting;
				pointerInteractionMovement = delta;
				x.set(delta / 200);
			}
		}}
	/>
</main>
