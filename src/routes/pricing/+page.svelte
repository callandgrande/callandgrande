<!-- src/routes/pricing/+page.svelte -->
<script>
	// Toggle for annual pricing - using standard let binding
	let isAnnual = false;

	// Function to toggle pricing
	function togglePricing() {
		isAnnual = !isAnnual;
	}
</script>

<!-- Page Header -->
<section class="px-4 py-16 md:py-24">
	<div class="container mx-auto max-w-4xl text-center">
		<h1 class="mb-6 text-4xl font-bold md:text-5xl">Simple, Transparent Pricing</h1>
		<p class="mx-auto max-w-2xl text-xl text-gray-300">
			Flexible options designed to meet your AI consulting needs, whether you're just starting or
			scaling up.
		</p>
	</div>
</section>

<!-- Pricing Toggle -->
<section class="mb-12 px-4">
	<div class="container mx-auto max-w-4xl">
		<div class="flex items-center justify-center space-x-4">
			<span class={!isAnnual ? 'font-medium' : 'text-gray-400'}>Monthly</span>
			<button
				type="button"
				aria-label="Toggle annual pricing"
				class="relative h-7 w-14 cursor-pointer rounded-full bg-purple-900/70 p-1"
				on:click={togglePricing}
			>
				<div
					class="absolute top-1/2 h-5 w-5 rounded-full bg-purple-600 transition-all duration-300"
					style={`transform: translateX(${isAnnual ? '28px' : '0px'}) translateY(-50%)`}
				></div>
			</button>
			<span class={isAnnual ? 'font-medium' : 'text-gray-400'}> Annual </span>
		</div>
	</div>
</section>

<!-- Pricing Plans -->
<section class="px-4 py-8 md:py-12">
	<div class="container mx-auto max-w-6xl">
		<div class="grid gap-8 md:grid-cols-3">
			<!-- Starter Plan -->
			<div
				class="flex flex-col rounded-lg border border-purple-900/30 bg-indigo-950/40 p-8 backdrop-blur-sm"
			>
				<h3 class="mb-2 text-xl font-bold">Starter</h3>
				<p class="mb-6 text-gray-300">For businesses beginning their AI journey.</p>
				<div class="mb-2 text-4xl font-bold">
					{isAnnual ? '$1,300' : '$300'}
					<span class="text-base font-normal text-gray-400">
						{isAnnual ? '/year' : '/month'}
					</span>
				</div>
				<p class="mb-6 text-sm text-gray-400">Single project implementation.</p>
				<ul class="mb-8 space-y-3">
					<li class="flex items-start">
						<div class="mt-0.5 mr-3 h-5 w-5 flex-shrink-0 rounded-full bg-purple-600"></div>
						<span>AI readiness assessment.</span>
					</li>
					<li class="flex items-start">
						<div class="mt-0.5 mr-3 h-5 w-5 flex-shrink-0 rounded-full bg-purple-600"></div>
						<span>Basic implementation plan.</span>
					</li>
					<li class="flex items-start">
						<div class="mt-0.5 mr-3 h-5 w-5 flex-shrink-0 rounded-full bg-purple-600"></div>
						<span>Application Deployment.</span>
					</li>
					<li class="flex items-start">
						<div class="mt-0.5 mr-3 h-5 w-5 flex-shrink-0 rounded-full bg-purple-600"></div>
						<span>40 hours consulting support.</span>
					</li>
					<li class="flex items-start">
						<div class="mt-0.5 mr-3 h-5 w-5 flex-shrink-0 rounded-full bg-purple-600"></div>
						<span>Email support anytime.</span>
					</li>
				</ul>
				<a
					href="/contact"
					class="mt-auto w-full rounded-md border border-indigo-600 px-6 py-3 text-center transition hover:border-purple-400"
				>
					Get Started
				</a>
			</div>

			<!-- Professional Plan -->
			<div
				class="relative flex flex-col rounded-lg border border-purple-600/50 bg-indigo-950/40 p-8 backdrop-blur-sm"
			>
				<h3 class="mb-2 text-xl font-bold">Professional</h3>
				<p class="mb-6 text-gray-300">For growing businesses with specific AI needs.</p>
				<div class="mb-2 text-4xl font-bold">
					{isAnnual ? '$5,000' : '$700'}
					<span class="text-base font-normal text-gray-400">
						{isAnnual ? '/year' : '/month'}
					</span>
				</div>
				<p class="mb-6 text-sm text-gray-400">Ongoing implementation & support.</p>
				<ul class="mb-8 space-y-3">
					<li class="flex items-start">
						<div class="mt-0.5 mr-3 h-5 w-5 flex-shrink-0 rounded-full bg-purple-600"></div>
						<span>All Starter features.</span>
					</li>
					<li class="flex items-start">
						<div class="mt-0.5 mr-3 h-5 w-5 flex-shrink-0 rounded-full bg-purple-600"></div>
						<span>Comprehensive strategy development.</span>
					</li>
					<li class="flex items-start">
						<div class="mt-0.5 mr-3 h-5 w-5 flex-shrink-0 rounded-full bg-purple-600"></div>
						<span>80 hours consulting support.</span>
					</li>
					<li class="flex items-start">
						<div class="mt-0.5 mr-3 h-5 w-5 flex-shrink-0 rounded-full bg-purple-600"></div>
						<span>Priority support with 24hr response.</span>
					</li>
					<li class="flex items-start">
						<div class="mt-0.5 mr-3 h-5 w-5 flex-shrink-0 rounded-full bg-purple-600"></div>
						<span>Quarterly progress reviews.</span>
					</li>
				</ul>
				<a
					href="/contact"
					class="mt-auto w-full rounded-md bg-purple-600 px-6 py-3 text-center transition hover:bg-purple-700"
				>
					Get Started
				</a>
			</div>

			<!-- Enterprise Plan -->
			<div
				class="flex flex-col rounded-lg border border-purple-900/30 bg-indigo-950/40 p-8 backdrop-blur-sm"
			>
				<h3 class="mb-2 text-xl font-bold">Enterprise</h3>
				<p class="mb-6 text-gray-300">For organizations with complex AI requirements.</p>
				<div class="mb-2 text-4xl font-bold">
					Custom
					<span class="text-base font-normal text-gray-400"></span>
				</div>
				<p class="mb-6 text-sm text-gray-400">Tailored to your specific needs.</p>
				<ul class="mb-8 space-y-3">
					<li class="flex items-start">
						<div class="mt-0.5 mr-3 h-5 w-5 flex-shrink-0 rounded-full bg-purple-600"></div>
						<span>All Professional features.</span>
					</li>
					<li class="flex items-start">
						<div class="mt-0.5 mr-3 h-5 w-5 flex-shrink-0 rounded-full bg-purple-600"></div>
						<span>Dedicated strategy team.</span>
					</li>
					<li class="flex items-start">
						<div class="mt-0.5 mr-3 h-5 w-5 flex-shrink-0 rounded-full bg-purple-600"></div>
						<span>Unlimited consulting hours.</span>
					</li>
					<li class="flex items-start">
						<div class="mt-0.5 mr-3 h-5 w-5 flex-shrink-0 rounded-full bg-purple-600"></div>
						<span>24/7 priority support.</span>
					</li>
					<li class="flex items-start">
						<div class="mt-0.5 mr-3 h-5 w-5 flex-shrink-0 rounded-full bg-purple-600"></div>
						<span>Monthly executive briefings.</span>
					</li>
				</ul>
				<a
					href="/contact"
					class="mt-auto w-full rounded-md border border-indigo-600 px-6 py-3 text-center transition hover:border-purple-400"
				>
					Contact Sales
				</a>
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
				<h3 class="mb-2 text-xl font-bold">Can I change plans later?</h3>
				<p class="text-gray-300">
					Yes, you can upgrade or downgrade your plan at any time. When upgrading, we'll prorate the
					remaining time on your current plan. For downgrades, changes take effect at the end of
					your current billing cycle.
				</p>
			</div>

			<!-- FAQ Item 2 -->
			<div class="rounded-lg border border-purple-900/30 bg-indigo-950/40 p-6 backdrop-blur-sm">
				<h3 class="mb-2 text-xl font-bold">What if my needs don't fit these plans?</h3>
				<p class="text-gray-300">
					Our Enterprise tier is fully customizable. Contact us to discuss your specific
					requirements, and we'll create a tailored solution that aligns with your business goals
					and budget.
				</p>
			</div>

			<!-- FAQ Item 3 -->
			<div class="rounded-lg border border-purple-900/30 bg-indigo-950/40 p-6 backdrop-blur-sm">
				<h3 class="mb-2 text-xl font-bold">Is there a minimum commitment period?</h3>
				<p class="text-gray-300">
					Monthly plans can be canceled anytime. Annual plans offer significant savings and come
					with a 30-day money-back guarantee, allowing you to try our services risk-free.
				</p>
			</div>
		</div>
	</div>
</section>
