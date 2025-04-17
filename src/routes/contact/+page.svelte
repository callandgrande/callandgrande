<!-- src/routes/contact/+page.svelte -->
<script>
	import { page } from '$app/stores';
	import { onMount } from 'svelte';

	// Form data
	let name = '';
	let email = '';
	let company = '';
	let message = '';
	let submitting = false;
	let submitted = false;
	let error = '';

	// Check for URL parameters on mount
	onMount(() => {
		// Get email from URL query parameter if it exists
		const urlParams = $page.url.searchParams;
		const emailParam = urlParams.get('email');

		if (emailParam) {
			email = emailParam;
		}
		
		// Check if form was submitted successfully (after redirect from FormSubmit)
		const thanksParam = urlParams.get('thanks');
		if (thanksParam === 'true') {
			submitted = true;
		}
	});

	// Form is now handled by FormSubmit directly
	// handleSubmit is only used for UI state management before form submission
	const handleSubmit = () => {
		submitting = true;
		// The actual submission is handled by the form's action
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
		<!-- Changed grid to flex and added justify-center to center the cards -->
		<div class="flex flex-col md:flex-row justify-center gap-8">
			<!-- Email -->
			<div
				class="rounded-lg border border-purple-900/30 bg-indigo-950/40 p-6 text-center backdrop-blur-sm md:w-1/4"
			>
				<div
					class="mx-auto mb-4 flex h-12 w-12 items-center justify-center rounded-full bg-indigo-600"
				>
					<div class="h-6 w-6 rounded-sm bg-white"></div>
					<!-- Simple email icon placeholder -->
				</div>
				<h3 class="mb-2 text-xl font-bold">Email Us</h3>
				<p class="mb-2 text-gray-300"><a href="mailto:info@callgran.com" class="hover:text-purple-400 transition">info@callgran.com</a></p>
				<p class="text-gray-300"><a href="mailto:support@callgran.com" class="hover:text-purple-400 transition">support@callgran.com</a></p>
			</div>

			<!-- Phone -->
			<div
				class="rounded-lg border border-purple-900/30 bg-indigo-950/40 p-6 text-center backdrop-blur-sm md:w-1/4"
			>
				<div
					class="mx-auto mb-4 flex h-12 w-12 items-center justify-center rounded-full bg-purple-500"
				>
					<div class="h-6 w-6 rounded-sm bg-white"></div>
					<!-- Simple phone icon placeholder -->
				</div>
				<h3 class="mb-2 text-xl font-bold">Call Us</h3>
				<p class="mb-2 text-gray-300"><a href="tel:+17575706407" class="hover:text-purple-400 transition">+1 (757) 570-6407</a></p>
				<p class="text-gray-300">24/7 Support</p>
			</div>
		</div>
	</div>
</section>

<!-- Contact Form and Map -->
<section class="px-4 py-16 backdrop-blur-sm md:py-24">
	<div class="container mx-auto max-w-6xl">
		<!-- Changed to center the form -->
		<div class="flex justify-center">
			<!-- Contact Form - Adjusted width and added mx-auto -->
			<div class="w-full max-w-xl">
				<h2 class="mb-8 text-3xl font-bold text-center">Send Us a Message</h2>

				{#if submitted}
					<div class="mb-8 rounded-lg border border-green-700/50 bg-green-950/70 p-8 text-center">
						<h3 class="mb-4 text-3xl font-bold">Thank You!</h3>
						<p class="text-xl">Your message has been sent. We'll get back to you shortly.</p>
					</div>
				{:else}
					<form 
						action="https://formsubmit.co/info@callgran.com" 
						method="POST" 
						on:submit={handleSubmit} 
						class="space-y-6"
					>
						<!-- FormSubmit Configuration -->
						<input type="hidden" name="_subject" value="New message from website contact form">
						<input type="hidden" name="_template" value="table">
						<input type="hidden" name="_next" value="https://callgran.com/contact?thanks=true">
						<input type="hidden" name="_autoresponse" value="Thank you for contacting us. We've received your message and will get back to you shortly.">
						<input type="hidden" name="_captcha" value="false">

						<!-- Name -->
						<div>
							<label for="name" class="mb-2 block text-sm font-medium">Your Name</label>
							<input
								type="text"
								id="name"
								name="name"
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
								name="email"
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
								name="company"
								bind:value={company}
								class="w-full rounded-md border border-indigo-800 bg-indigo-950/40 px-4 py-3 focus:ring-2 focus:ring-purple-600 focus:outline-none"
							/>
						</div>

						<!-- Message -->
						<div>
							<label for="message" class="mb-2 block text-sm font-medium">Your Message</label>
							<textarea
								id="message"
								name="message"
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