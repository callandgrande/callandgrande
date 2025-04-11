<script>
	import Globe from '$lib/components/Globe.svelte';
	import { goto } from '$app/navigation';
	
	// Email state
	let contactEmail = '';
	
	// Function to handle form submission
	function handleContactRequest() {
		if (contactEmail) {
			// Navigate to contact page with email as query parameter
			goto(`/contact?email=${encodeURIComponent(contactEmail)}`);
		}
	}
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
					<p class="mt-6 text-gray-400">Starting at $300.00</p>
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

	<!-- Features Section -->
	<section class="container mx-auto px-4 py-16 md:px-6 md:py-24">
		<h2 class="mb-10 text-center text-2xl font-bold md:mb-16 md:text-3xl">Our Services</h2>
		<div class="grid gap-8 md:grid-cols-2 md:gap-12 lg:grid-cols-3">			
			<!-- Feature 1 -->
			<div
				class="rounded-lg border border-purple-900/30 bg-indigo-950/60 p-6 backdrop-blur-sm md:p-8"
			>
				<div class="mb-4 flex justify-center items-center text-4xl md:mb-6">🧠</div>
				<h3 class="mb-3 text-lg font-bold md:mb-4 md:text-xl text-center">AI Strategy</h3>
				<p class="text-sm text-gray-300 md:text-base text-justify">
					Our team builds a practical, results-driven AI roadmap tailored to your goals—so AI becomes a tool that drives revenue, efficiency, and growth.
				</p>
			</div>
			<!-- Feature 2 -->
			<div
				class="rounded-lg border border-purple-900/30 bg-indigo-950/60 p-6 backdrop-blur-sm md:p-8"
			>
				<div class="mb-4 flex justify-center items-center text-4xl md:mb-6">📊</div>
				<h3 class="mb-3 text-lg font-bold md:mb-4 md:text-xl text-center">Data Science & Engineering</h3>
				<p class="text-sm text-gray-300 md:text-base text-justify">
					Harness the power of your data. From data management to model training, we build robust, efficient pipelines that help you identify edge cases, gain insights, and accelerate deployment.
				</p>
			</div>
			<!-- Feature 3 -->
			<div
				class="rounded-lg border border-purple-900/30 bg-indigo-950/60 p-6 backdrop-blur-sm md:p-8"
			>
				<div class="mb-4 flex justify-center items-center text-4xl md:mb-6">🔄</div>
				<h3 class="mb-3 text-lg font-bold md:mb-4 md:text-xl text-center">End-to-End AI Implementation</h3>
				<p class="text-sm text-gray-300 md:text-base text-justify">
					From ideation to execution, we offer full-cycle AI implementation services. Our team ensures seamless integration into your existing systems for maximum impact.
				</p>
			</div>
		</div>
		
		<!-- Second row - centered in desktop -->
		<div class="grid gap-8 mt-8 md:grid-cols-2 md:gap-12 md:mx-auto md:max-w-2xl lg:max-w-4xl">
			<!-- Feature 4 -->
			<div
				class="rounded-lg border border-purple-900/30 bg-indigo-950/60 p-6 backdrop-blur-sm md:p-8">
				<div class="mb-4 flex justify-center items-center text-4xl md:mb-6">💻</div>
				<h3 class="mb-3 text-lg font-bold md:mb-4 md:text-xl text-center">Custom Web & Software Development</h3>
				<p class="text-sm text-gray-300 md:text-base text-justify">
					Need a platform for your AI? We design and build scalable web apps and software that power your AI solutions and streamline your digital operations.
				</p>
			</div>
			<!-- Feature 5 -->
			<div
				class="rounded-lg border border-purple-900/30 bg-indigo-950/60 p-6 backdrop-blur-sm md:p-8">
				<div class="mb-4 flex justify-center items-center text-4xl md:mb-6">🔧</div>
				<h3 class="mb-3 text-lg font-bold md:mb-4 md:text-xl text-center">24/7 DevOps & Support</h3>
				<p class="text-sm text-gray-300 md:text-base text-justify">
					Our dedicated DevOps team is available around the clock to provide project support, system monitoring, and continuous optimization—ensuring your AI infrastructure runs smoothly at all times.
				</p>
			</div>
		</div>
	</section>


	<!-- CTA Section - Updated with form submission -->
	<section class="container mx-auto px-4 py-16 text-center md:px-6 md:py-24">
		<h2 class="mb-6 text-2xl font-bold md:mb-8 md:text-3xl">
			Ready to transform your business with AI?
		</h2>
		<div class="mx-auto max-w-md">
			<form on:submit|preventDefault={handleContactRequest} class="flex flex-col sm:flex-row">
				<input
					type="email"
					placeholder="Enter your email"
					bind:value={contactEmail}
					required
					class="mb-2 w-full flex-grow rounded-md border border-indigo-800 bg-indigo-950/40 px-4 py-3 focus:ring-2 focus:ring-purple-600 focus:outline-none sm:mb-0 sm:rounded-l-md sm:rounded-r-none"
				/>
				<button
					type="submit"
					class="w-full flex-shrink-0 rounded-md bg-purple-600 px-6 py-3 whitespace-nowrap transition hover:bg-purple-700 sm:w-auto sm:rounded-l-none sm:whitespace-normal"
				>
					Get in touch
				</button>
			</form>
			<p class="mt-4 text-sm text-gray-400 md:text-base">
				— Empower your team with Call & Grande today.
			</p>
		</div>
	</section>
</div>