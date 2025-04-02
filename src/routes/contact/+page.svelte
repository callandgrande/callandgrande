<!-- src/routes/contact/+page.svelte -->
<script>
	// Simple form handling - you can expand this as needed
	let name = '';
	let email = '';
	let company = '';
	let message = '';
	let submitting = false;
	let submitted = false;
	let error = '';

	const handleSubmit = () => {
		submitting = true;

		// Simulate form submission
		setTimeout(() => {
			submitting = false;
			submitted = true;

			// Reset form
			name = '';
			email = '';
			company = '';
			message = '';
		}, 1000);
	};
</script>

<!-- Page Header -->
<section class="px-4 py-16 md:py-24">
	<div class="container mx-auto max-w-4xl text-center">
		<h1 class="mb-6 text-4xl font-bold md:text-5xl">Get in Touch</h1>
		<p class="mx-auto max-w-2xl text-xl text-gray-300">
			Ready to explore how AI can transform your business? We're here to help you navigate the
			possibilities.
		</p>
	</div>
</section>

<!-- Contact Information -->
<section class="px-4 py-8 md:py-12">
	<div class="container mx-auto max-w-6xl">
		<div class="grid gap-8 md:grid-cols-3">
			<!-- Address -->
			<div
				class="rounded-lg border border-purple-900/30 bg-indigo-950/40 p-6 text-center backdrop-blur-sm"
			>
				<div
					class="mx-auto mb-4 flex h-12 w-12 items-center justify-center rounded-full bg-purple-600"
				>
					<div class="h-6 w-6 rounded-sm bg-white"></div>
					<!-- Simple location icon placeholder -->
				</div>
				<h3 class="mb-2 text-xl font-bold">Our Office</h3>
				<p class="text-gray-300">
					123 Tech Avenue<br />
					San Francisco, CA 94107<br />
					United States
				</p>
			</div>

			<!-- Email -->
			<div
				class="rounded-lg border border-purple-900/30 bg-indigo-950/40 p-6 text-center backdrop-blur-sm"
			>
				<div
					class="mx-auto mb-4 flex h-12 w-12 items-center justify-center rounded-full bg-indigo-600"
				>
					<div class="h-6 w-6 rounded-sm bg-white"></div>
					<!-- Simple email icon placeholder -->
				</div>
				<h3 class="mb-2 text-xl font-bold">Email Us</h3>
				<p class="mb-2 text-gray-300">info@callandgrande.com</p>
				<p class="text-gray-300">support@callandgrande.com</p>
			</div>

			<!-- Phone -->
			<div
				class="rounded-lg border border-purple-900/30 bg-indigo-950/40 p-6 text-center backdrop-blur-sm"
			>
				<div
					class="mx-auto mb-4 flex h-12 w-12 items-center justify-center rounded-full bg-purple-500"
				>
					<div class="h-6 w-6 rounded-sm bg-white"></div>
					<!-- Simple phone icon placeholder -->
				</div>
				<h3 class="mb-2 text-xl font-bold">Call Us</h3>
				<p class="mb-2 text-gray-300">+1 (415) 555-0123</p>
				<p class="text-gray-300">Monday - Friday, 9am - 5pm PST</p>
			</div>
		</div>
	</div>
</section>

<!-- Contact Form and Map -->
<section class="px-4 py-16 backdrop-blur-sm md:py-24">
	<div class="container mx-auto max-w-6xl">
		<div class="flex flex-col gap-16 lg:flex-row">
			<!-- Contact Form -->
			<div class="lg:w-1/2">
				<h2 class="mb-8 text-3xl font-bold">Send Us a Message</h2>

				{#if submitted}
					<div class="mb-8 rounded-lg border border-green-600 bg-green-500/20 p-6">
						<h3 class="mb-2 text-xl font-bold">Thank You!</h3>
						<p>Your message has been sent. We'll get back to you shortly.</p>
					</div>
				{:else}
					<form on:submit|preventDefault={handleSubmit} class="space-y-6">
						<!-- Name -->
						<div>
							<label for="name" class="mb-2 block text-sm font-medium">Your Name</label>
							<input
								type="text"
								id="name"
								bind:value={name}
								required
								class="w-full rounded-md border border-indigo-800 bg-indigo-950/40 px-4 py-3 focus:ring-2 focus:ring-purple-600 focus:outline-none"
							/>
						</div>

						<!-- Email -->
						<div>
							<label for="email" class="mb-2 block text-sm font-medium">Email Address</label>
							<input
								type="email"
								id="email"
								bind:value={email}
								required
								class="w-full rounded-md border border-indigo-800 bg-indigo-950/40 px-4 py-3 focus:ring-2 focus:ring-purple-600 focus:outline-none"
							/>
						</div>

						<!-- Company -->
						<div>
							<label for="company" class="mb-2 block text-sm font-medium">Company</label>
							<input
								type="text"
								id="company"
								bind:value={company}
								class="w-full rounded-md border border-indigo-800 bg-indigo-950/40 px-4 py-3 focus:ring-2 focus:ring-purple-600 focus:outline-none"
							/>
						</div>

						<!-- Message -->
						<div>
							<label for="message" class="mb-2 block text-sm font-medium">Your Message</label>
							<textarea
								id="message"
								bind:value={message}
								required
								rows="5"
								class="w-full rounded-md border border-indigo-800 bg-indigo-950/40 px-4 py-3 focus:ring-2 focus:ring-purple-600 focus:outline-none"
							></textarea>
						</div>

						<!-- Submit Button -->
						<button
							type="submit"
							disabled={submitting}
							class="w-full rounded-md bg-purple-600 px-6 py-3 text-center transition hover:bg-purple-700 disabled:opacity-75"
						>
							{submitting ? 'Sending...' : 'Send Message'}
						</button>
					</form>
				{/if}
			</div>

			<!-- Map Placeholder -->
			<div class="lg:w-1/2">
				<h2 class="mb-8 text-3xl font-bold">Find Us</h2>
				<div
					class="flex h-96 w-full items-center justify-center rounded-lg bg-gradient-to-br from-indigo-800 to-purple-900"
				>
					<div class="text-center">
						<div class="mx-auto mb-4 h-16 w-16">
							<!-- Simple map pin placeholder -->
							<div class="mx-auto h-8 w-8 rounded-full bg-purple-600"></div>
							<div class="mx-auto -mt-3 h-8 w-2 bg-purple-600"></div>
						</div>
						<p class="text-lg font-medium">Map Location</p>
						<p class="text-sm text-gray-300">123 Tech Avenue, San Francisco</p>
					</div>
				</div>
			</div>
		</div>
	</div>
</section>

<!-- FAQ Section -->
<section class="px-4 py-16 md:py-24">
	<div class="container mx-auto max-w-4xl">
		<h2 class="mb-12 text-center text-3xl font-bold">Frequently Asked Questions</h2>

		<div class="space-y-6">
			<!-- FAQ Item 1 -->
			<div class="rounded-lg border border-purple-900/30 bg-indigo-950/40 p-6 backdrop-blur-sm">
				<h3 class="mb-2 text-xl font-bold">How soon can you start working with us?</h3>
				<p class="text-gray-300">
					We typically begin with a discovery call within 1-2 business days of your inquiry. After
					our initial consultation, we can often start a project within two weeks, depending on the
					scope and our current capacity.
				</p>
			</div>

			<!-- FAQ Item 2 -->
			<div class="rounded-lg border border-purple-900/30 bg-indigo-950/40 p-6 backdrop-blur-sm">
				<h3 class="mb-2 text-xl font-bold">
					Do you work with startups or just enterprise clients?
				</h3>
				<p class="text-gray-300">
					We work with organizations of all sizes. For startups, we offer specialized packages that
					focus on establishing the right AI foundation to scale. Our goal is to meet you where you
					are in your AI journey.
				</p>
			</div>

			<!-- FAQ Item 3 -->
			<div class="rounded-lg border border-purple-900/30 bg-indigo-950/40 p-6 backdrop-blur-sm">
				<h3 class="mb-2 text-xl font-bold">What industries do you specialize in?</h3>
				<p class="text-gray-300">
					While our expertise spans multiple sectors, we have deep experience in healthcare,
					finance, retail, and manufacturing. Our diverse team brings industry-specific knowledge to
					each project we undertake.
				</p>
			</div>
		</div>
	</div>
</section>

<!-- Newsletter Subscribe -->
<section class="px-4 py-16 text-center backdrop-blur-sm md:py-24">
	<div class="container mx-auto max-w-3xl">
		<h2 class="mb-6 text-3xl font-bold">Stay Updated</h2>
		<p class="mb-8 text-xl text-gray-300">
			Subscribe to our newsletter for the latest AI insights and industry updates.
		</p>
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
					Subscribe
				</button>
			</div>
		</div>
	</div>
</section>
