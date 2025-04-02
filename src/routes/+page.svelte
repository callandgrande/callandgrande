<script>
	import Globe from '$lib/components/Globe.svelte';
</script>

<!-- Main content -->
<div class="flex flex-col">
	<!-- Hero Section - With improved spacing between text and globe -->
	<section
		class="px-4 py-12 md:px-6 md:py-0"
		style="min-height: 80vh; display: flex; align-items: center;"
	>
		<div class="container mx-auto max-w-7xl">
			<div class="flex flex-col-reverse gap-16 md:flex-row md:items-center md:gap-28">
				<div class="mt-8 md:mt-0 md:w-5/12">
					<h2 class="text-4xl leading-tight font-bold md:text-5xl">
						Unlock the
						<span
							class="bg-gradient-to-r from-indigo-400 to-purple-500 bg-clip-text text-transparent"
							>potential</span
						>
						of your AI strategy
					</h2>
					<p class="mt-4 mb-6 text-lg text-gray-300 md:text-xl">
						Call & Grande offers specialized AI consulting services and professional implementation
						to ensure the correct fit of AI in your business processes.
					</p>
					<div class="flex flex-col space-y-4 sm:flex-row sm:space-y-0 sm:space-x-4">
						<a
							href="/pricing"
							class="w-full rounded-md bg-purple-600 px-6 py-3 text-center transition hover:bg-purple-700 sm:w-auto"
						>
							Get Started
						</a>
						<a
							href="/contact"
							class="w-full rounded-md border border-indigo-600 px-6 py-3 text-center transition hover:border-purple-400 sm:w-auto"
						>
							Talk to Sales
						</a>
					</div>
					<p class="mt-6 text-gray-400">Starting at $1500.00</p>
				</div>
				<div class="flex items-center justify-center md:w-7/12 md:pl-12">
					<div class="relative h-[400px] w-full max-w-[400px] md:h-[500px] md:max-w-[500px]">
						<Globe
							class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 scale-110 transform"
						/>
					</div>
				</div>
			</div>
		</div>
	</section>

	<!-- Trusted By Section -->
	<section class="px-4 py-8 md:px-6">
		<div class="container mx-auto">
			<p class="mb-6 text-center text-sm text-gray-400 md:text-base">
				Trusted by the world's leading organizations
			</p>
			<div class="flex flex-wrap justify-center gap-4 md:gap-8 lg:gap-16">
				<!-- Company logos placeholders - responsive sizes -->
				<div class="h-6 w-16 rounded-md bg-indigo-900/60 backdrop-blur-sm md:h-8 md:w-24"></div>
				<div class="h-6 w-16 rounded-md bg-indigo-900/60 backdrop-blur-sm md:h-8 md:w-24"></div>
				<div class="h-6 w-16 rounded-md bg-indigo-900/60 backdrop-blur-sm md:h-8 md:w-24"></div>
				<div class="h-6 w-16 rounded-md bg-indigo-900/60 backdrop-blur-sm md:h-8 md:w-24"></div>
				<div class="h-6 w-16 rounded-md bg-indigo-900/60 backdrop-blur-sm md:h-8 md:w-24"></div>
			</div>
		</div>
	</section>

	<!-- Features Section -->
	<section class="container mx-auto px-4 py-16 md:px-6 md:py-24">
		<h2 class="mb-10 text-center text-2xl font-bold md:mb-16 md:text-3xl">Our Services</h2>
		<div class="grid gap-8 md:grid-cols-2 md:gap-12 lg:grid-cols-3">
			<!-- Feature 1 -->
			<div
				class="rounded-lg border border-purple-900/30 bg-indigo-950/60 p-6 backdrop-blur-sm md:p-8"
			>
				<div class="mb-4 h-10 w-10 rounded-md bg-purple-600 md:mb-6 md:h-12 md:w-12"></div>
				<h3 class="mb-3 text-lg font-bold md:mb-4 md:text-xl">AI Strategy</h3>
				<p class="text-sm text-gray-300 md:text-base">
					Develop a tailored AI implementation roadmap that aligns with your business goals and
					existing processes.
				</p>
			</div>
			<!-- Feature 2 -->
			<div
				class="rounded-lg border border-purple-900/30 bg-indigo-950/60 p-6 backdrop-blur-sm md:p-8"
			>
				<div class="mb-4 h-10 w-10 rounded-md bg-indigo-600 md:mb-6 md:h-12 md:w-12"></div>
				<h3 class="mb-3 text-lg font-bold md:mb-4 md:text-xl">Data Engineering</h3>
				<p class="text-sm text-gray-300 md:text-base">
					Manage large data sets with ease, identify edge cases, and train models efficiently to
					deploy faster.
				</p>
			</div>
			<!-- Feature 3 -->
			<div
				class="rounded-lg border border-purple-900/30 bg-indigo-950/60 p-6 backdrop-blur-sm md:col-span-2 md:p-8 lg:col-span-1"
			>
				<div class="mb-4 h-10 w-10 rounded-md bg-purple-500 md:mb-6 md:h-12 md:w-12"></div>
				<h3 class="mb-3 text-lg font-bold md:mb-4 md:text-xl">Implementation</h3>
				<p class="text-sm text-gray-300 md:text-base">
					Professional implementation and 24/7 DevOps project support to ensure the correct fit of
					AI in your business.
				</p>
			</div>
		</div>
	</section>

	<!-- CTA Section - Fixed button alignment -->
	<section class="container mx-auto px-4 py-16 text-center md:px-6 md:py-24">
		<h2 class="mb-6 text-2xl font-bold md:mb-8 md:text-3xl">
			Ready to transform your business with AI?
		</h2>
		<div class="mx-auto max-w-md">
			<div class="flex flex-col sm:flex-row">
				<input
					type="email"
					placeholder="Enter your email"
					class="mb-2 w-full flex-grow rounded-md border border-indigo-800 bg-indigo-950/40 px-4 py-3 focus:ring-2 focus:ring-purple-600 focus:outline-none sm:mb-0 sm:rounded-l-md sm:rounded-r-none"
				/>
				<button
					class="w-full flex-shrink-0 rounded-md bg-purple-600 px-6 py-3 whitespace-nowrap transition hover:bg-purple-700 sm:w-auto sm:rounded-l-none sm:whitespace-normal"
				>
					Get in touch
				</button>
			</div>
			<p class="mt-4 text-sm text-gray-400 md:text-base">
				— Empower your team with Call & Grande today.
			</p>
		</div>
	</section>
</div>
