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
<section class="bg-indigo-950/30 px-4 py-16 backdrop-blur-sm md:py-24">
	<div class="container mx-auto max-w-6xl">
		<div class="flex flex-col items-center gap-16 md:flex-row">
			<div class="order-2 md:order-1 md:w-1/2">
				<h2 class="mb-6 text-3xl font-bold">Our Story</h2>
				<p class="mb-4 text-gray-300">
					Founded in 2023, Call & Grande emerged from the recognition that businesses need more than
					just AI tools—they need strategic guidance to integrate AI effectively.
				</p>
				<p class="mb-4 text-gray-300">
					Our founders, Joseph Call and Martin Grande, combined their expertise in data science and
					business strategy to create a consultancy that bridges the gap between cutting-edge AI
					technology and practical business applications.
				</p>
				<p class="text-gray-300">
					Today, we've helped over 50 companies across diverse industries implement AI solutions
					that drive real business value, focusing on tailored strategies that align with each
					client's unique goals and challenges.
				</p>
			</div>
			<div class="order-1 mb-8 md:order-2 md:mb-0 md:w-1/2">
				<!-- Placeholder for team image -->
				<div
					class="flex h-80 w-full items-center justify-center rounded-lg bg-gradient-to-br from-indigo-800 to-purple-900 md:h-96"
				>
					<div class="text-center">
						<div class="mx-auto mb-4 h-16 w-16 rounded-full bg-purple-600"></div>
						<p class="text-lg font-medium">Our Team</p>
					</div>
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
				<div class="mb-6 h-12 w-12 rounded-md bg-purple-600"></div>
				<h3 class="mb-4 text-xl font-bold">Practical Innovation</h3>
				<p class="text-gray-300">
					We believe AI should solve real problems. We focus on implementations that deliver
					tangible business value, not just flashy technology.
				</p>
			</div>

			<!-- Value 2 -->
			<div class="rounded-lg border border-purple-900/30 bg-indigo-950/40 p-8 backdrop-blur-sm">
				<div class="mb-6 h-12 w-12 rounded-md bg-indigo-600"></div>
				<h3 class="mb-4 text-xl font-bold">Ethical Excellence</h3>
				<p class="text-gray-300">
					We commit to responsible AI practices, ensuring our solutions respect privacy, reduce
					bias, and consider the broader social impact of artificial intelligence.
				</p>
			</div>

			<!-- Value 3 -->
			<div class="rounded-lg border border-purple-900/30 bg-indigo-950/40 p-8 backdrop-blur-sm">
				<div class="mb-6 h-12 w-12 rounded-md bg-purple-500"></div>
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
<section class="bg-indigo-950/30 px-4 py-16 backdrop-blur-sm md:py-24">
	<div class="container mx-auto max-w-6xl">
		<h2 class="mb-12 text-center text-3xl font-bold">Meet Our Leadership</h2>
		<div class="grid gap-8 md:grid-cols-2 lg:grid-cols-4">
			<!-- Team Member 1 -->
			<div class="text-center">
				<!-- Placeholder for team member photo -->
				<div
					class="mx-auto mb-4 flex h-40 w-40 items-center justify-center rounded-full bg-gradient-to-br from-indigo-800 to-purple-900"
				>
					<div class="h-10 w-10 rounded-full bg-purple-600"></div>
				</div>
				<h3 class="text-xl font-bold">Sarah Call</h3>
				<p class="text-gray-400">Co-Founder & CEO</p>
			</div>

			<!-- Team Member 2 -->
			<div class="text-center">
				<!-- Placeholder for team member photo -->
				<div
					class="mx-auto mb-4 flex h-40 w-40 items-center justify-center rounded-full bg-gradient-to-br from-indigo-800 to-purple-900"
				>
					<div class="h-10 w-10 rounded-full bg-indigo-600"></div>
				</div>
				<h3 class="text-xl font-bold">Miguel Grande</h3>
				<p class="text-gray-400">Co-Founder & CTO</p>
			</div>

			<!-- Team Member 3 -->
			<div class="text-center">
				<!-- Placeholder for team member photo -->
				<div
					class="mx-auto mb-4 flex h-40 w-40 items-center justify-center rounded-full bg-gradient-to-br from-indigo-800 to-purple-900"
				>
					<div class="h-10 w-10 rounded-full bg-purple-500"></div>
				</div>
				<h3 class="text-xl font-bold">Elena Chen</h3>
				<p class="text-gray-400">AI Strategy Director</p>
			</div>

			<!-- Team Member 4 -->
			<div class="text-center">
				<!-- Placeholder for team member photo -->
				<div
					class="mx-auto mb-4 flex h-40 w-40 items-center justify-center rounded-full bg-gradient-to-br from-indigo-800 to-purple-900"
				>
					<div class="h-10 w-10 rounded-full bg-indigo-500"></div>
				</div>
				<h3 class="text-xl font-bold">David Park</h3>
				<p class="text-gray-400">Implementation Lead</p>
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
				href="#"
				class="w-full rounded-md bg-purple-600 px-6 py-3 text-center transition hover:bg-purple-700 sm:w-auto"
			>
				Schedule a Consultation
			</a>
			<a
				href="#"
				class="w-full rounded-md border border-indigo-600 px-6 py-3 text-center transition hover:border-purple-400 sm:w-auto"
			>
				View Our Case Studies
			</a>
		</div>
	</div>
</section>
