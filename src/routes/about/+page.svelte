<!-- src/routes/about/+page.svelte -->
<script>
	// You can add any necessary imports or logic here
</script>

<!-- Page Header -->
<section class="px-4 py-16 md:py-24">
	<div class="container mx-auto max-w-4xl text-center">
		<h1 class="mb-6 text-4xl font-bold md:text-5xl">About Call & Grande</h1>
		<p class="mx-auto max-w-2xl text-xl text-gray-300">
			We help businesses navigate the complex world of artificial intelligence with practical
			solutions and expert guidance.
		</p>
	</div>
</section>

<!-- Our Story Section -->
<section class="px-4 py-16 backdrop-blur-sm md:py-24">
	<div class="container mx-auto max-w-6xl">
		<div class="flex flex-col items-center gap-16 md:flex-row">
			<div class="order-2 md:order-1 md:w-1/2">
				<h2 class="mb-6 text-3xl font-bold">Our Story</h2>
				<p class="mb-4 text-gray-300">
					Founded in 2025, Call & Grande was born from a simple insight: businesses don't just need
					AI—they need a strategy for AI. Recognizing this critical gap, our co-founders combined
					their expertise in data science and business strategy to build a consultancy that
					transforms cutting-edge AI into real-world business value.
				</p>
				<p class="mb-4 text-gray-300">
					At Call & Grande, we specialize in turning complex AI concepts into measurable results.
					With a foundation in advanced research and hands-on industry experience, we help
					organizations harness emerging technologies before they become mainstream—giving our
					clients a powerful competitive edge.
				</p>
				<p class="text-gray-300">
					We don't just implement tools; we deliver end-to-end solutions rooted in rigorous
					research, state-of-the-art AI capabilities, and sharp strategic insight. Our mission is
					simple: to solve your toughest challenges with intelligent, actionable solutions that move
					your business forward.
				</p>
			</div>
			<div class="order-1 mb-8 md:order-2 md:mb-0 md:w-1/2">
				<!-- Placeholder for team image -->
				<div class="text-center">
					<img src="images/logo.png" alt="logo" />
				</div>
			</div>
		</div>
	</div>
</section>

<!-- Our Values Section -->
<section class="px-4 py-16 md:py-24">
	<div class="container mx-auto max-w-6xl">
		<h2 class="mb-12 text-center text-3xl font-bold">Our Values</h2>
		<div class="grid gap-8 md:grid-cols-3">
			<!-- Value 1 -->
			<div class="rounded-lg border border-purple-900/30 bg-indigo-950/40 p-8 backdrop-blur-sm">
				<h3 class="mb-4 text-xl font-bold">Practical Innovation</h3>
				<p class="text-gray-300">
					We believe AI should solve real problems. We focus on implementations that deliver
					tangible business value, not just flashy technology.
				</p>
			</div>

			<!-- Value 2 -->
			<div class="rounded-lg border border-purple-900/30 bg-indigo-950/40 p-8 backdrop-blur-sm">
				<h3 class="mb-4 text-xl font-bold">Ethical Excellence</h3>
				<p class="text-gray-300">
					We commit to responsible AI practices, ensuring our solutions respect privacy, reduce
					bias, and consider the broader social impact of artificial intelligence.
				</p>
			</div>

			<!-- Value 3 -->
			<div class="rounded-lg border border-purple-900/30 bg-indigo-950/40 p-8 backdrop-blur-sm">
				<h3 class="mb-4 text-xl font-bold">Client Partnership</h3>
				<p class="text-gray-300">
					We view ourselves as strategic partners in your AI journey, focusing on knowledge transfer
					and sustainable approaches that grow with your business.
				</p>
			</div>
		</div>
	</div>
</section>

<!-- Team Section -->
<section class="px-4 py-16 backdrop-blur-sm md:py-24">
	<div class="container mx-auto max-w-6xl">
		<h2 class="mb-12 text-center text-3xl font-bold">Meet Our Leadership</h2>
		<div class="grid gap-8 md:grid-cols-2 lg:grid-cols-2">
			<!-- Team Member 1 -->
			<div class="text-center">
				<!-- Placeholder for team member photo -->
				<div class="mx-auto mb-4 flex h-40 w-40 items-center justify-center rounded-full">
					<img src="images/headshots/joseph.jpg" alt="Joseph Headshot" class="rounded-full" />
				</div>
				<h3 class="text-xl font-bold">Joseph Call</h3>
				<p class="text-gray-400">Co-Founder & Managing Partner</p>
				<!-- LinkedIn Icon -->
				<div class="mt-2">
					<a
						href="https://www.linkedin.com/in/jbcallv/"
						target="_blank"
						rel="noopener noreferrer"
						class="inline-block text-indigo-400 transition hover:text-purple-400"
					>
						<svg
							xmlns="http://www.w3.org/2000/svg"
							class="h-6 w-6"
							fill="currentColor"
							viewBox="0 0 24 24"
						>
							<path
								d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z"
							/>
						</svg>
					</a>
				</div>
			</div>

			<!-- Team Member 2 -->
			<div class="text-center">
				<!-- Placeholder for team member photo -->
				<div class="mx-auto mb-4 flex h-40 w-40 items-center justify-center rounded-full">
					<img src="images/headshots/alvaro.jpg" alt="Alvaro Headshot" class="rounded-full" />
				</div>
				<h3 class="text-xl font-bold">Alvaro Martin Grande</h3>
				<p class="text-gray-400">Co-Founder</p>
				<!-- LinkedIn Icon -->
				<div class="mt-2">
					<a
						href="https://www.linkedin.com/in/alvaromartingrande/"
						target="_blank"
						rel="noopener noreferrer"
						class="inline-block text-indigo-400 transition hover:text-purple-400"
					>
						<svg
							xmlns="http://www.w3.org/2000/svg"
							class="h-6 w-6"
							fill="currentColor"
							viewBox="0 0 24 24"
						>
							<path
								d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z"
							/>
						</svg>
					</a>
				</div>
			</div>
		</div>
	</div>
</section>

<!-- Contact CTA -->
<section class="px-4 py-16 text-center md:py-24">
	<div class="container mx-auto max-w-3xl">
		<h2 class="mb-6 text-3xl font-bold">Ready to Transform Your Business?</h2>
		<p class="mb-8 text-xl text-gray-300">
			Let's discuss how our AI consulting services can help you achieve your goals.
		</p>
		<div class="flex flex-col justify-center gap-4 sm:flex-row">
			<a
				href="/contact"
				class="w-full rounded-md bg-purple-600 px-6 py-3 text-center transition hover:bg-purple-700 sm:w-auto"
			>
				Schedule a Consultation
			</a>
			<a
				href="/solutions"
				class="w-full rounded-md border border-indigo-600 px-6 py-3 text-center transition hover:border-purple-400 sm:w-auto"
			>
				View Our Case Studies
			</a>
		</div>
	</div>
</section>
