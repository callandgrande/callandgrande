<!-- src/routes/solutions/+page.svelte -->
<script>
	// You can add any necessary imports or logic here
</script>

<!-- Page Header -->
<section class="px-4 py-16 md:py-24">
	<div class="container mx-auto max-w-4xl text-center">
		<h1 class="mb-6 text-4xl font-bold md:text-5xl">Our AI Solutions</h1>
		<p class="mx-auto max-w-2xl text-xl text-gray-300">
			We help businesses implement practical AI strategies that drive measurable results and create
			lasting competitive advantages.
		</p>
	</div>
</section>

<!-- Solution Categories -->
<section class="px-4 py-16">
	<div class="container mx-auto max-w-6xl">
		<div class="grid gap-12 md:grid-cols-2">
			<!-- Strategy & Assessment -->
			<div class="rounded-lg border border-purple-900/30 bg-indigo-950/40 p-8 backdrop-blur-sm">
				<div class="mb-6 h-12 w-12 rounded-md bg-purple-600"></div>
				<h2 class="mb-4 text-2xl font-bold">Strategy & Assessment</h2>
				<p class="mb-4 text-gray-300">
					Our strategic assessment identifies opportunities where AI can create the most value for
					your business. We evaluate your data readiness, technical capabilities, and organizational
					structure.
				</p>
				<ul class="space-y-2 text-gray-300">
					<li class="flex items-start">
						<div class="mt-1.5 mr-2 h-1 w-1 flex-shrink-0 rounded-full bg-purple-600"></div>
						<span>AI Readiness Assessment</span>
					</li>
					<li class="flex items-start">
						<div class="mt-1.5 mr-2 h-1 w-1 flex-shrink-0 rounded-full bg-purple-600"></div>
						<span>Technology Roadmapping</span>
					</li>
					<li class="flex items-start">
						<div class="mt-1.5 mr-2 h-1 w-1 flex-shrink-0 rounded-full bg-purple-600"></div>
						<span>ROI & Business Case Development</span>
					</li>
				</ul>
			</div>

			<!-- Data Engineering -->
			<div class="rounded-lg border border-purple-900/30 bg-indigo-950/40 p-8 backdrop-blur-sm">
				<div class="mb-6 h-12 w-12 rounded-md bg-indigo-600"></div>
				<h2 class="mb-4 text-2xl font-bold">Data Engineering</h2>
				<p class="mb-4 text-gray-300">
					We build the foundation for successful AI by preparing and structuring your data. Our team
					ensures your data assets are accessible, clean, and ready for advanced analytics and
					machine learning.
				</p>
				<ul class="space-y-2 text-gray-300">
					<li class="flex items-start">
						<div class="mt-1.5 mr-2 h-1 w-1 flex-shrink-0 rounded-full bg-indigo-600"></div>
						<span>Data Architecture Design</span>
					</li>
					<li class="flex items-start">
						<div class="mt-1.5 mr-2 h-1 w-1 flex-shrink-0 rounded-full bg-indigo-600"></div>
						<span>ETL Pipeline Development</span>
					</li>
					<li class="flex items-start">
						<div class="mt-1.5 mr-2 h-1 w-1 flex-shrink-0 rounded-full bg-indigo-600"></div>
						<span>Data Quality & Governance</span>
					</li>
				</ul>
			</div>

			<!-- AI Model Development -->
			<div class="rounded-lg border border-purple-900/30 bg-indigo-950/40 p-8 backdrop-blur-sm">
				<div class="mb-6 h-12 w-12 rounded-md bg-purple-500"></div>
				<h2 class="mb-4 text-2xl font-bold">AI Model Development</h2>
				<p class="mb-4 text-gray-300">
					We build custom AI models that address your specific business challenges. Our development
					process balances performance, interpretability, and efficiency to deliver solutions that
					work in real-world conditions.
				</p>
				<ul class="space-y-2 text-gray-300">
					<li class="flex items-start">
						<div class="mt-1.5 mr-2 h-1 w-1 flex-shrink-0 rounded-full bg-purple-500"></div>
						<span>Custom Machine Learning Models</span>
					</li>
					<li class="flex items-start">
						<div class="mt-1.5 mr-2 h-1 w-1 flex-shrink-0 rounded-full bg-purple-500"></div>
						<span>Large Language Model Fine-tuning</span>
					</li>
					<li class="flex items-start">
						<div class="mt-1.5 mr-2 h-1 w-1 flex-shrink-0 rounded-full bg-purple-500"></div>
						<span>Computer Vision Solutions</span>
					</li>
				</ul>
			</div>

			<!-- Implementation & Integration -->
			<div class="rounded-lg border border-purple-900/30 bg-indigo-950/40 p-8 backdrop-blur-sm">
				<div class="mb-6 h-12 w-12 rounded-md bg-indigo-500"></div>
				<h2 class="mb-4 text-2xl font-bold">Implementation & Integration</h2>
				<p class="mb-4 text-gray-300">
					We bridge the gap between AI concepts and operational reality. Our team ensures AI
					solutions integrate seamlessly with your existing systems and workflows while providing
					reliable monitoring and maintenance.
				</p>
				<ul class="space-y-2 text-gray-300">
					<li class="flex items-start">
						<div class="mt-1.5 mr-2 h-1 w-1 flex-shrink-0 rounded-full bg-indigo-500"></div>
						<span>API Development & Integration</span>
					</li>
					<li class="flex items-start">
						<div class="mt-1.5 mr-2 h-1 w-1 flex-shrink-0 rounded-full bg-indigo-500"></div>
						<span>MLOps & Continuous Deployment</span>
					</li>
					<li class="flex items-start">
						<div class="mt-1.5 mr-2 h-1 w-1 flex-shrink-0 rounded-full bg-indigo-500"></div>
						<span>Performance Monitoring</span>
					</li>
				</ul>
			</div>
		</div>
	</div>
</section>

<!-- Industry Solutions -->
<section class="px-4 py-16 backdrop-blur-sm md:py-24">
	<div class="container mx-auto max-w-6xl">
		<h2 class="mb-12 text-center text-3xl font-bold">Industry-Specific Solutions</h2>

		<div class="grid gap-8 md:grid-cols-3">
			<!-- Healthcare -->
			<div class="rounded-lg border border-purple-900/30 bg-indigo-950/50 p-6 backdrop-blur-sm">
				<h3 class="mb-3 text-xl font-bold">Healthcare</h3>
				<p class="text-gray-300">
					Improve patient outcomes and operational efficiency with AI solutions for diagnostic
					support, treatment optimization, and administrative automation.
				</p>
			</div>

			<!-- Finance -->
			<div class="rounded-lg border border-purple-900/30 bg-indigo-950/50 p-6 backdrop-blur-sm">
				<h3 class="mb-3 text-xl font-bold">Finance</h3>
				<p class="text-gray-300">
					Enhance risk management, automate compliance processes, and deliver personalized customer
					experiences with our financial services AI solutions.
				</p>
			</div>

			<!-- Retail -->
			<div class="rounded-lg border border-purple-900/30 bg-indigo-950/50 p-6 backdrop-blur-sm">
				<h3 class="mb-3 text-xl font-bold">Retail</h3>
				<p class="text-gray-300">
					Transform customer engagement, optimize inventory management, and create seamless
					omnichannel experiences with retail-focused AI implementations.
				</p>
			</div>

			<!-- Manufacturing -->
			<div class="rounded-lg border border-purple-900/30 bg-indigo-950/50 p-6 backdrop-blur-sm">
				<h3 class="mb-3 text-xl font-bold">Manufacturing</h3>
				<p class="text-gray-300">
					Increase production efficiency, improve quality control, and enable predictive maintenance
					with manufacturing-specific AI solutions.
				</p>
			</div>

			<!-- Media & Entertainment -->
			<div class="rounded-lg border border-purple-900/30 bg-indigo-950/50 p-6 backdrop-blur-sm">
				<h3 class="mb-3 text-xl font-bold">Media & Entertainment</h3>
				<p class="text-gray-300">
					Enhance content creation, optimize recommendation systems, and improve audience engagement
					with AI solutions for media companies.
				</p>
			</div>

			<!-- Professional Services -->
			<div class="rounded-lg border border-purple-900/30 bg-indigo-950/50 p-6 backdrop-blur-sm">
				<h3 class="mb-3 text-xl font-bold">Professional Services</h3>
				<p class="text-gray-300">
					Streamline document processing, automate routine tasks, and generate data-driven insights
					with AI solutions tailored for service organizations.
				</p>
			</div>
		</div>
	</div>
</section>

<!-- Case Studies Preview -->
<section class="px-4 py-16 md:py-24">
	<div class="container mx-auto max-w-6xl">
		<h2 class="mb-12 text-center text-3xl font-bold">Success Stories</h2>

		<div class="grid gap-8 md:grid-cols-2 lg:grid-cols-3">
			<!-- Case Study 1 -->
			<div class="overflow-hidden rounded-lg border border-purple-900/30 bg-indigo-950/40">
				<!-- Case study image placeholder -->
				<div
					class="flex h-48 items-center justify-center bg-gradient-to-r from-indigo-800 to-purple-900"
				>
					<div
						class="flex h-16 w-16 items-center justify-center rounded-full bg-purple-600/50 backdrop-blur-sm"
					>
						<div class="h-8 w-8 rounded-full bg-purple-600"></div>
					</div>
				</div>
				<div class="p-6">
					<h3 class="mb-2 text-xl font-bold">Healthcare Provider Reduces Costs by 32%</h3>
					<p class="mb-4 text-gray-300">
						We helped a regional healthcare network implement AI-driven patient flow optimization
						and predictive resource allocation.
					</p>
					<a href="#" class="font-medium text-purple-400 hover:text-purple-300">Read case study →</a
					>
				</div>
			</div>

			<!-- Case Study 2 -->
			<div class="overflow-hidden rounded-lg border border-purple-900/30 bg-indigo-950/40">
				<!-- Case study image placeholder -->
				<div
					class="flex h-48 items-center justify-center bg-gradient-to-r from-indigo-800 to-purple-900"
				>
					<div
						class="flex h-16 w-16 items-center justify-center rounded-full bg-indigo-600/50 backdrop-blur-sm"
					>
						<div class="h-8 w-8 rounded-full bg-indigo-600"></div>
					</div>
				</div>
				<div class="p-6">
					<h3 class="mb-2 text-xl font-bold">Retail Chain Improves Inventory Accuracy</h3>
					<p class="mb-4 text-gray-300">
						Our demand forecasting model helped a national retailer reduce stockouts by 45% while
						decreasing excess inventory costs.
					</p>
					<a href="#" class="font-medium text-purple-400 hover:text-purple-300">Read case study →</a
					>
				</div>
			</div>

			<!-- Case Study 3 -->
			<div class="overflow-hidden rounded-lg border border-purple-900/30 bg-indigo-950/40">
				<!-- Case study image placeholder -->
				<div
					class="flex h-48 items-center justify-center bg-gradient-to-r from-indigo-800 to-purple-900"
				>
					<div
						class="flex h-16 w-16 items-center justify-center rounded-full bg-purple-500/50 backdrop-blur-sm"
					>
						<div class="h-8 w-8 rounded-full bg-purple-500"></div>
					</div>
				</div>
				<div class="p-6">
					<h3 class="mb-2 text-xl font-bold">Financial Institution Enhances Fraud Detection</h3>
					<p class="mb-4 text-gray-300">
						We developed a real-time anomaly detection system that reduced fraud losses by 67% while
						minimizing false positives.
					</p>
					<a href="#" class="font-medium text-purple-400 hover:text-purple-300">Read case study →</a
					>
				</div>
			</div>
		</div>
	</div>
</section>

<!-- CTA Section -->
<section class="px-4 py-16 text-center backdrop-blur-sm md:py-24">
	<div class="container mx-auto max-w-3xl">
		<h2 class="mb-6 text-3xl font-bold">Ready to Transform Your Business?</h2>
		<p class="mb-8 text-xl text-gray-300">
			Schedule a free consultation to discuss how our AI solutions can address your specific
			challenges.
		</p>
		<div class="flex flex-col justify-center gap-4 sm:flex-row">
			<a
				href="/contact"
				class="w-full rounded-md bg-purple-600 px-6 py-3 text-center transition hover:bg-purple-700 sm:w-auto"
			>
				Schedule a Consultation
			</a>
			<a
				href="/pricing"
				class="w-full rounded-md border border-indigo-600 px-6 py-3 text-center transition hover:border-purple-400 sm:w-auto"
			>
				View Pricing
			</a>
		</div>
	</div>
</section>
