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
				radius: Math.random() * 1.5 + 1.5,
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
	<div class="absolute inset-0 bg-gradient-to-br from-gray-900 via-indigo-950 to-purple-950"></div>

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
					<div class="md:w-1/3">
						<div class="mb-6">
							<h3
								class="bg-gradient-to-r from-indigo-400 to-purple-500 bg-clip-text text-2xl font-bold text-transparent"
							>
								Call & Grande
							</h3>
						</div>
						<p class="mb-6 max-w-xs text-gray-300">
							Specialized AI consulting services helping businesses implement practical AI
							strategies that drive measurable results.
						</p>
						<!-- Social Links -->
						<div class="flex space-x-4">
							<a
								href="#"
								class="flex h-10 w-10 items-center justify-center rounded-full bg-indigo-900/60 transition hover:bg-purple-600"
							>
								<div class="h-5 w-5 rounded-full bg-gray-300"></div>
							</a>
							<a
								href="#"
								class="flex h-10 w-10 items-center justify-center rounded-full bg-indigo-900/60 transition hover:bg-purple-600"
							>
								<div class="h-5 w-5 rounded-full bg-gray-300"></div>
							</a>
							<a
								href="#"
								class="flex h-10 w-10 items-center justify-center rounded-full bg-indigo-900/60 transition hover:bg-purple-600"
							>
								<div class="h-5 w-5 rounded-full bg-gray-300"></div>
							</a>
						</div>
					</div>

					<!-- Navigation Links -->
					<div class="grid grid-cols-2 gap-8 md:w-2/3 md:grid-cols-4">
						<div>
							<h4 class="mb-4 text-lg font-semibold text-white">Company</h4>
							<ul class="space-y-3">
								<li>
									<a href="/about" class="text-gray-300 transition hover:text-purple-400">About</a>
								</li>
								<li>
									<a href="/careers" class="text-gray-300 transition hover:text-purple-400"
										>Careers</a
									>
								</li>
								<li>
									<a href="/blog" class="text-gray-300 transition hover:text-purple-400">Blog</a>
								</li>
							</ul>
						</div>
						<div>
							<h4 class="mb-4 text-lg font-semibold text-white">Solutions</h4>
							<ul class="space-y-3">
								<li>
									<a
										href="/solutions#strategy"
										class="text-gray-300 transition hover:text-purple-400">Strategy</a
									>
								</li>
								<li>
									<a
										href="/solutions#development"
										class="text-gray-300 transition hover:text-purple-400">Development</a
									>
								</li>
								<li>
									<a
										href="/solutions#implementation"
										class="text-gray-300 transition hover:text-purple-400">Implementation</a
									>
								</li>
							</ul>
						</div>
						<div>
							<h4 class="mb-4 text-lg font-semibold text-white">Resources</h4>
							<ul class="space-y-3">
								<li>
									<a href="/resources" class="text-gray-300 transition hover:text-purple-400"
										>Case Studies</a
									>
								</li>
								<li>
									<a href="/resources#guides" class="text-gray-300 transition hover:text-purple-400"
										>Guides</a
									>
								</li>
								<li>
									<a href="/resources#faq" class="text-gray-300 transition hover:text-purple-400"
										>FAQ</a
									>
								</li>
							</ul>
						</div>
						<div>
							<h4 class="mb-4 text-lg font-semibold text-white">Contact</h4>
							<ul class="space-y-3">
								<li>
									<a href="/contact" class="text-gray-300 transition hover:text-purple-400"
										>Get in Touch</a
									>
								</li>
								<li>
									<a
										href="mailto:info@callandgrande.com"
										class="text-gray-300 transition hover:text-purple-400">info@callandgrande.com</a
									>
								</li>
								<li>
									<a href="tel:+14155550123" class="text-gray-300 transition hover:text-purple-400"
										>+1 (415) 555-0123</a
									>
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
						<a href="/privacy" class="text-gray-300 transition hover:text-purple-400"
							>Privacy Policy</a
						>
						<a href="/terms" class="text-gray-300 transition hover:text-purple-400"
							>Terms of Service</a
						>
					</div>
				</div>
			</div>
		</footer>
	</div>
</main>
