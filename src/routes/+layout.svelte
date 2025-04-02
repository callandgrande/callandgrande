<script>
	import '../app.css';
	import { onMount } from 'svelte';

	let { children } = $props();
	let canvas;
	let dots = [];

	// Animation for the dots
	onMount(() => {
		if (typeof window === 'undefined') return;

		const ctx = canvas.getContext('2d');
		const width = (canvas.width = window.innerWidth);
		const height = (canvas.height = window.innerHeight);

		// Create dots
		for (let i = 0; i < 100; i++) {
			dots.push({
				x: Math.random() * width,
				y: Math.random() * height,
				radius: Math.random() * 1.5 + 0.5,
				vx: Math.random() * 0.5 - 0.25,
				vy: Math.random() * 0.5 - 0.25,
				opacity: Math.random() * 0.5 + 0.1
			});
		}

		function animate() {
			ctx.clearRect(0, 0, width, height);

			// Draw and update dots
			for (let i = 0; i < dots.length; i++) {
				const dot = dots[i];

				dot.x += dot.vx;
				dot.y += dot.vy;

				// Wrap around edges
				if (dot.x < 0) dot.x = width;
				if (dot.x > width) dot.x = 0;
				if (dot.y < 0) dot.y = height;
				if (dot.y > height) dot.y = 0;

				// Draw the dot
				ctx.beginPath();
				ctx.arc(dot.x, dot.y, dot.radius, 0, Math.PI * 2);
				ctx.fillStyle = `rgba(255, 255, 255, ${dot.opacity})`;
				ctx.fill();
			}

			requestAnimationFrame(animate);
		}

		animate();

		// Handle resize
		const handleResize = () => {
			canvas.width = window.innerWidth;
			canvas.height = window.innerHeight;
		};

		window.addEventListener('resize', handleResize);

		return () => {
			window.removeEventListener('resize', handleResize);
		};
	});
</script>

<main class="relative min-h-screen overflow-hidden text-white">
	<!-- Gradient background -->
	<div class="absolute inset-0 bg-gradient-to-br from-gray-900 via-indigo-950 to-purple-900"></div>

	<!-- Animated dots canvas - now fixed position to cover entire scrollable area -->
	<canvas bind:this={canvas} class="fixed inset-0 z-0 opacity-50"></canvas>

	<!-- Content -->
	<div class="relative z-10">
		<!-- Navigation -->
		<nav class="container mx-auto flex items-center justify-between px-6 py-4">
			<div class="flex items-center">
				<h1 class="text-xl font-bold">Call & Grande</h1>
			</div>
			<div class="hidden space-x-8 md:flex">
				<a href="#" class="transition hover:text-purple-400">Solutions</a>
				<a href="#" class="transition hover:text-purple-400">Pricing</a>
				<a href="#" class="transition hover:text-purple-400">About</a>
				<a href="#" class="transition hover:text-purple-400">Contact</a>
			</div>
			<div class="flex items-center space-x-4">
				<a href="#" class="transition hover:text-purple-400">Sign In</a>
				<a href="#" class="rounded-md bg-purple-600 px-4 py-2 transition hover:bg-purple-700"
					>Get Started</a
				>
			</div>
		</nav>

		<!-- Main content -->
		{@render children()}

		<!-- Footer -->
		<footer class="bg-gray-800/80 py-12 backdrop-blur-sm">
			<div class="container mx-auto px-6">
				<div class="flex flex-col justify-between md:flex-row">
					<div class="mb-8 md:mb-0">
						<h3 class="mb-4 text-xl font-bold">Call & Grande</h3>
						<p class="max-w-xs text-gray-400">
							Specialized AI consulting services and professional implementation.
						</p>
					</div>
					<div class="grid grid-cols-2 gap-8 md:grid-cols-4">
						<div>
							<h4 class="mb-4 text-lg font-semibold">Company</h4>
							<ul class="space-y-2">
								<li><a href="#" class="text-gray-400 hover:text-white">About</a></li>
								<li><a href="#" class="text-gray-400 hover:text-white">Careers</a></li>
								<li><a href="#" class="text-gray-400 hover:text-white">Blog</a></li>
							</ul>
						</div>
						<div>
							<h4 class="mb-4 text-lg font-semibold">Services</h4>
							<ul class="space-y-2">
								<li><a href="#" class="text-gray-400 hover:text-white">Strategy</a></li>
								<li><a href="#" class="text-gray-400 hover:text-white">Implementation</a></li>
								<li><a href="#" class="text-gray-400 hover:text-white">Support</a></li>
							</ul>
						</div>
						<div>
							<h4 class="mb-4 text-lg font-semibold">Resources</h4>
							<ul class="space-y-2">
								<li><a href="#" class="text-gray-400 hover:text-white">Documentation</a></li>
								<li><a href="#" class="text-gray-400 hover:text-white">Case Studies</a></li>
								<li><a href="#" class="text-gray-400 hover:text-white">Guides</a></li>
							</ul>
						</div>
						<div>
							<h4 class="mb-4 text-lg font-semibold">Contact</h4>
							<ul class="space-y-2">
								<li><a href="#" class="text-gray-400 hover:text-white">Email</a></li>
								<li><a href="#" class="text-gray-400 hover:text-white">Support</a></li>
								<li><a href="#" class="text-gray-400 hover:text-white">Social</a></li>
							</ul>
						</div>
					</div>
				</div>
				<div
					class="mt-12 flex flex-col items-center justify-between border-t border-gray-700 pt-8 md:flex-row"
				>
					<p class="text-gray-400">© 2025 Call & Grande. All rights reserved.</p>
					<div class="mt-4 flex space-x-6 md:mt-0">
						<a href="#" class="text-gray-400 hover:text-white">Privacy Policy</a>
						<a href="#" class="text-gray-400 hover:text-white">Terms of Service</a>
					</div>
				</div>
			</div>
		</footer>
	</div>
</main>
