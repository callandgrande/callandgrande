<script>
	import '../app.css';
	import { onMount } from 'svelte';

	let { children } = $props();
	let canvas;
	let dots = [];
	let animationFrame;

	// Animation for the dots
	onMount(() => {
		if (typeof window === 'undefined') return;

		const ctx = canvas.getContext('2d');
		const width = (canvas.width = window.innerWidth);
		const height = (canvas.height = window.innerHeight);

		// Function to create dots
		function createDots() {
			dots = [];
			for (let i = 0; i < 100; i++) {
				dots.push({
					x: Math.random() * width,
					y: Math.random() * height,
					radius: Math.random() * 1.5 + 1.5,
					vx: Math.random() * 0.5 - 0.25,
					vy: Math.random() * 0.5 - 0.25,
					opacity: Math.random() * 0.5 + 0.1
				});
			}
		}

		// Initial creation of dots
		createDots();

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

			animationFrame = requestAnimationFrame(animate);
		}

		animate();

		// Handle resize
		const handleResize = () => {
			// Cancel the current animation frame to prevent multiple animations
			if (animationFrame) {
				cancelAnimationFrame(animationFrame);
			}
			
			// Update canvas dimensions
			canvas.width = window.innerWidth;
			canvas.height = window.innerHeight;
			
			// Recreate dots with new dimensions
			createDots();
			
			// Restart animation
			animate();
		};

		window.addEventListener('resize', handleResize);

		return () => {
			window.removeEventListener('resize', handleResize);
			if (animationFrame) {
				cancelAnimationFrame(animationFrame);
			}
		};
	});
</script>

<main class="relative min-h-screen overflow-hidden text-white">
	<!-- Gradient background -->
	<div class="absolute inset-0 bg-gradient-to-br from-gray-900 via-indigo-950 to-purple-950"></div>

	<!-- Animated dots canvas - now fixed position to cover entire scrollable area -->
	<canvas bind:this={canvas} class="fixed inset-0 z-0 opacity-50"></canvas>

	<!-- Content -->
	<div class="relative z-10">
		<!-- Navigation -->
		<nav class="container mx-auto flex items-center justify-between px-6 py-4">
			<a href="/" class="flex items-center">
				<img src="images/logo.png" width="120" alt="logo" />
			</a>
			<div class="hidden space-x-8 md:flex">
				<a href="/solutions" class="transition hover:text-purple-400">Solutions</a>
				<a href="/pricing" class="transition hover:text-purple-400">Pricing</a>
				<a href="/about" class="transition hover:text-purple-400">About</a>
				<a href="/contact" class="transition hover:text-purple-400">Contact</a>
			</div>
			<div class="flex items-center space-x-4">
				<a href="/contact" class="rounded-md bg-purple-600 px-4 py-2 transition hover:bg-purple-700"
					>Get Started</a
				>
			</div>
		</nav>

		<!-- Main content -->
		{@render children()}

		<!-- Footer with elegant separator line -->
		<footer class="py-16 backdrop-blur-sm">
			<!-- Option 1: Fading line separator -->
			<div class="container mx-auto mb-16 px-6">
				<div class="relative">
					<div class="absolute inset-0 flex items-center">
						<div
							class="h-px w-full border-t border-purple-700/70 bg-gradient-to-r from-transparent via-purple-500/50 to-transparent"
						></div>
					</div>
				</div>
			</div>

			<div class="container mx-auto px-6">
				<!-- Main Footer Content -->
				<div class="flex flex-col justify-between gap-12 md:flex-row">
					<!-- Company Info -->
					<div class="md:w-1/2">
						<div class="mb-6">
							<img src="images/logo.png" width="150" alt="logo" />
						</div>
						<p class="mb-6 max-w-xs text-gray-300">
							Specialized AI consulting services helping businesses implement practical AI
							strategies that drive measurable results.
						</p>
					</div>

					<!-- Navigation Links - Now aligned to the right -->
					<div class="grid grid-cols-2 gap-8 md:w-1/2 md:grid-cols-2 md:justify-items-end">
						<div class="text-right">
							<h4 class="mb-4 text-lg font-semibold text-white">Company</h4>
							<ul class="space-y-3">
								<li>
									<a href="/pricing" class="text-gray-300 transition hover:text-purple-400">Pricing</a>
								</li>
								<li>
									<a href="/about" class="text-gray-300 transition hover:text-purple-400">About</a>
								</li>
							</ul>
						</div>
						<div class="text-right">
							<h4 class="mb-4 text-lg font-semibold text-white">Contact</h4>
							<ul class="space-y-3">
								<li>
									<a href="/contact" class="text-gray-300 transition hover:text-purple-400"
										>Get in Touch</a
									>
								</li>
								<li>
									<a href="mailto:info@callgran.com" class="text-gray-300 transition hover:text-purple-400">
										info@callgran.com
									</a>
								</li>
								<li>
									<a href="tel:+16187035999" class="text-gray-300 transition hover:text-purple-400">
										+1 (618) 703-5999
									</a>
								</li>
							</ul>
						</div>
					</div>
				</div>

				<!-- Footer Bottom -->
				<div
					class="mt-16 flex flex-col items-center justify-between border-t border-indigo-800/30 pt-8 md:flex-row"
				>
					<p class="mb-4 text-gray-400 md:mb-0">© 2025 Call & Grande. All rights reserved.</p>
					<div class="flex space-x-8">
					</div>
				</div>
			</div>
		</footer>
	</div>
</main>