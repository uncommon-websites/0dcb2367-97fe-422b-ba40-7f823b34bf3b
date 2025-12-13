<script lang="ts">
	import { onMount } from 'svelte';

	let email = '';
	
	const faqs = [
		{ question: "Does Hyprnote record my meetings?", answer: "Hyprnote transcribes your meetings locally on your device. No audio ever leaves your computer, ensuring complete privacy." },
		{ question: "How does on-device transcription work?", answer: "Hyprnote uses advanced AI models that run entirely on your device. This means faster processing, no internet required, and zero data sent to the cloud." },
		{ question: "Can I use Hyprnote with my handwritten notes?", answer: "Yes! Hyprnote uniquely combines AI transcription with your handwritten notes, creating comprehensive meeting documentation." },
		{ question: "Is Hyprnote compliant with GDPR, HIPAA, and other regulations?", answer: "Because all transcription happens on-device and no data is transmitted, Hyprnote inherently supports compliance requirements for privacy-sensitive industries." },
		{ question: "What if I'm in a regulated industry like healthcare or finance?", answer: "Hyprnote is designed specifically for compliance-heavy roles where cloud-based meeting bots create data leak risks. Everything stays on your device." },
		{ question: "Does Hyprnote work offline?", answer: "Yes! Since all processing happens on your device, you can transcribe meetings without an internet connection." },
		{ question: "How accurate is the transcription?", answer: "Hyprnote uses state-of-the-art speech recognition models optimized for meeting contexts, delivering highly accurate transcriptions even with multiple speakers." },
		{ question: "Can other meeting participants see that I'm using Hyprnote?", answer: "No. Unlike meeting bots that join calls and notify everyone, Hyprnote works silently on your device without disrupting the meeting." },
		{ question: "What happens to my meeting data?", answer: "Your meeting transcriptions and notes stay on your device. You have complete control over your data - export, delete, or sync as you choose." },
		{ question: "Does Hyprnote integrate with my calendar?", answer: "Yes, Hyprnote can integrate with your calendar to automatically organize meeting notes and summaries." }
	];
</script>

<div class="min-h-screen bg-dark-bg text-white font-sans selection:bg-brand-green selection:text-dark-bg">
	
	<!-- Announcement Banner -->
	<div class="w-full bg-dark-bg py-3 text-center text-[10px] tracking-widest uppercase border-b border-white/5">
		<span class="text-gray-400">Privacy-First</span> <span class="text-brand-primary-light">Meeting Notes</span> <span class="text-gray-400">That Never Leave Your Device</span>
	</div>

	<!-- Navigation -->
	<nav class="flex items-center justify-between px-6 py-5 max-w-7xl mx-auto">
		<div class="flex items-center gap-8">
			<a href="/" class="flex items-center gap-2">
				<svg xmlns="http://www.w3.org/2000/svg" width="120" height="25" viewBox="0 0 1269 263" fill="none" class="h-6 w-auto">
					<path d="M150.925 5.28271V257.674H85.2832V151.661H65.6414V257.674H0V5.28271H65.6414V95.5497H85.2832V5.28271H150.925Z" fill="currentColor"/>
					<path d="M317.134 5.28271L269.267 166.322V257.674H208.46V166.322L162.302 5.28271H222.602C232.025 54.5482 237.337 87.7054 238.538 104.74C242.171 77.806 248.265 44.6632 256.819 5.28271H317.12H317.134Z" fill="currentColor"/>
					<path d="M328.352 5.28271H394.456C412.332 5.28271 426.083 6.68658 435.694 9.4943C445.305 12.302 452.528 16.3544 457.362 21.6515C462.197 26.9485 465.468 33.3744 467.19 40.9003C468.898 48.4407 469.767 60.1057 469.767 75.8956V97.8798C469.767 113.988 468.102 125.74 464.773 133.107C461.444 140.488 455.336 146.147 446.449 150.098C437.561 154.049 425.938 156.017 411.594 156.017H393.979V257.66H328.337V5.28271H328.352ZM393.993 48.4696V112.7C395.861 112.801 397.482 112.859 398.828 112.859C404.849 112.859 409.047 111.383 411.377 108.416C413.722 105.449 414.88 99.2981 414.88 89.9342V69.2091C414.88 60.5833 413.534 54.9679 410.827 52.3773C408.12 49.7866 402.504 48.4841 393.993 48.4841V48.4696Z" fill="currentColor"/>
					<path d="M983.507 153.079C983.507 178.435 982.913 196.396 981.712 206.947C980.511 217.497 976.776 227.136 970.48 235.863C964.198 244.591 955.687 251.292 944.99 255.981C934.279 260.655 921.817 263 907.574 263C893.331 263 881.925 260.786 871.171 256.371C860.416 251.957 851.761 245.329 845.218 236.5C838.661 227.672 834.768 218.047 833.523 207.656C832.278 197.264 831.656 179.072 831.656 153.093V109.907C831.656 84.5502 832.249 66.5894 833.451 56.0387C834.637 45.4881 838.386 35.8492 844.683 27.1221C850.965 18.3949 859.461 11.694 870.172 7.01932C880.883 2.3446 893.346 0 907.589 0C921.093 0 933.237 2.21434 943.992 6.62855C954.746 11.0428 963.402 17.6713 969.944 26.4997C976.501 35.3281 980.395 44.9526 981.64 55.344C982.884 65.7355 983.507 83.9278 983.507 109.907V153.093V153.079ZM917.865 70.1353C917.865 58.3978 917.214 50.8864 915.911 47.6011C914.609 44.3302 911.931 42.6948 907.878 42.6948C904.448 42.6948 901.828 44.0263 900.004 46.6748C898.18 49.3234 897.283 57.1387 897.283 70.1353V187.987C897.283 202.648 897.876 211.679 899.078 215.109C900.264 218.54 903.058 220.247 907.415 220.247C911.772 220.247 914.739 218.279 915.984 214.328C917.228 210.377 917.851 200.97 917.851 186.106V70.1353H917.865Z" fill="currentColor"/>
					<path d="M1140.19 5.28223V55.7924H1101.21V257.688H1035.57V55.7924H996.751V5.28223H1140.19Z" fill="currentColor"/>
					<path d="M1155.17 5.28223H1264.63V55.7924H1220.81V103.654H1261.82V151.675H1220.81V207.178H1269V257.688H1155.19V5.28223H1155.17Z" fill="currentColor"/>
					<path d="M605.855 132.195L630.563 5.23926L523.669 5.28268H488.641V257.674H554.283V143.874C563.329 143.874 568.916 145.481 571.044 148.708C573.172 151.936 574.243 160.301 574.243 173.804V257.674H630.244L645.877 132.18H605.87L605.855 132.195ZM574.229 81.8294C574.229 92.9445 572.752 99.5152 569.785 101.556C566.818 103.582 561.65 104.595 554.268 104.595V48.4696C561.853 48.4696 567.078 49.7142 569.944 52.2035C572.81 54.6929 574.229 59.9465 574.229 67.95V81.8294Z" fill="currentColor"/>
					<path d="M752.278 5.28281V118.938L715.484 5.28281H708.102V5.21045L670.295 5.22492L653.823 77.1259L654.055 78.1245H693.512L630.577 257.689H635.195H660.612H708.218H715.484V142.948L749.629 257.689H807.165V5.28281H752.278Z" fill="currentColor"/>
				</svg>
			</a>
		</div>
		<a href="#contact" class="bg-white text-dark-bg px-6 py-2.5 rounded text-sm font-medium hover:bg-gray-100 transition-colors">Get Early Access</a>
	</nav>

	<!-- Hero Section -->
	<section class="pt-20 pb-32 px-4 text-center max-w-5xl mx-auto relative z-10">
		<h1 class="text-5xl md:text-7xl font-serif mb-6 tracking-tight">Meeting Notes That Never Leave Your Device</h1>
		<p class="text-gray-400 text-lg md:text-xl mb-10 max-w-2xl mx-auto font-light">
			On-device AI transcription combined with your handwritten notes. No cloud. No bots. No data leaks.
		</p>

		<div class="flex flex-col sm:flex-row items-center justify-center gap-2 mb-4 max-w-md mx-auto">
			<input 
				type="email" 
				placeholder="Email" 
				bind:value={email}
				class="w-full sm:w-64 bg-dark-surface border border-white/10 rounded px-4 py-2.5 text-sm text-white placeholder-gray-500 focus:outline-none focus:border-brand-primary-light/50 transition-colors"
			/>
			<button class="w-full sm:w-auto bg-white text-dark-bg px-6 py-2.5 rounded text-sm font-medium hover:bg-gray-100 transition-colors">
				Join Waitlist
			</button>
		</div>
		
		<a href="#contact" class="text-xs text-gray-500 hover:text-gray-400 underline decoration-gray-700 underline-offset-4">for compliance teams and enterprise access</a>
	</section>

	<!-- Hero Image/Video Placeholder -->
	<div class="relative max-w-6xl mx-auto px-4 -mt-16 mb-32">
		<div class="rounded-lg overflow-hidden border border-white/10 shadow-2xl bg-dark-surface aspect-[16/9] relative group cursor-pointer">
			<!-- Meeting Notes UI Mockup -->
			<div class="absolute inset-0 bg-white text-black text-sm overflow-hidden">
				<!-- Header -->
				<div class="w-full h-12 bg-gray-50 border-b border-gray-200 flex items-center justify-between px-4">
					<div class="flex items-center gap-3">
						<div class="w-2 h-2 rounded-full bg-red-500"></div>
						<span class="font-medium text-sm">Q4 Strategy Meeting - Dec 15, 2024</span>
					</div>
					<div class="flex items-center gap-2 text-xs text-gray-500">
						<div class="flex items-center gap-1">
							<div class="w-2 h-2 rounded-full bg-green-500"></div>
							<span>Transcribing locally</span>
						</div>
					</div>
				</div>
				
				<!-- Content Area -->
				<div class="flex h-[calc(100%-3rem)]">
					<!-- Transcription Panel -->
					<div class="w-1/2 border-r border-gray-200 p-6 overflow-hidden">
						<div class="text-xs font-semibold text-gray-500 mb-3 uppercase tracking-wide">Live Transcription</div>
						<div class="space-y-3 text-xs">
							<div class="flex gap-2">
								<span class="font-semibold text-gray-700 min-w-[60px]">Sarah:</span>
								<span class="text-gray-600">Let's review the Q4 numbers. Revenue is tracking 15% above forecast...</span>
							</div>
							<div class="flex gap-2">
								<span class="font-semibold text-gray-700 min-w-[60px]">Michael:</span>
								<span class="text-gray-600">That's great. What about the new product launch timeline?</span>
							</div>
							<div class="flex gap-2">
								<span class="font-semibold text-gray-700 min-w-[60px]">Sarah:</span>
								<span class="text-gray-600">We're on track for January 15th. Beta testing starts next week...</span>
							</div>
							<div class="flex gap-2 opacity-60">
								<span class="font-semibold text-gray-700 min-w-[60px]">Alex:</span>
								<span class="text-gray-600">I have concerns about the compliance review process...</span>
							</div>
						</div>
					</div>
					
					<!-- Notes Panel -->
					<div class="w-1/2 p-6 bg-gray-50">
						<div class="text-xs font-semibold text-gray-500 mb-3 uppercase tracking-wide">Your Notes</div>
						<div class="space-y-2 text-xs text-gray-700">
							<div class="flex items-start gap-2">
								<div class="w-1 h-1 rounded-full bg-gray-400 mt-1.5"></div>
								<span>Q4 revenue: +15% vs forecast</span>
							</div>
							<div class="flex items-start gap-2">
								<div class="w-1 h-1 rounded-full bg-gray-400 mt-1.5"></div>
								<span>Product launch: Jan 15</span>
							</div>
							<div class="flex items-start gap-2">
								<div class="w-1 h-1 rounded-full bg-gray-400 mt-1.5"></div>
								<span>Beta testing next week</span>
							</div>
							<div class="flex items-start gap-2">
								<div class="w-1 h-1 rounded-full bg-yellow-400 mt-1.5"></div>
								<span class="text-yellow-700">⚠️ Follow up: compliance review</span>
							</div>
						</div>
					</div>
				</div>
			</div>

			<!-- Play Button Overlay -->
			<div class="absolute inset-0 flex items-center justify-center bg-black/20">
				<div class="w-20 h-20 bg-white rounded-full flex items-center justify-center pl-1 transition-transform group-hover:scale-105 shadow-2xl">
					<svg width="24" height="24" viewBox="0 0 24 24" fill="black" xmlns="http://www.w3.org/2000/svg">
						<path d="M5 3L19 12L5 21V3Z" />
					</svg>
				</div>
			</div>
		</div>
		<!-- Gradient Glows -->
		<div class="absolute -top-20 -left-20 w-96 h-96 bg-brand-primary/10 rounded-full blur-[100px] -z-10"></div>
		<div class="absolute -bottom-20 -right-20 w-96 h-96 bg-brand-primary-dark/10 rounded-full blur-[100px] -z-10"></div>
	</div>

	<!-- Privacy First Section -->
	<section class="bg-white text-dark-bg py-24">
		<div class="max-w-6xl mx-auto px-6 grid md:grid-cols-2 gap-16 items-center">
			<div>
				<h2 class="text-4xl md:text-5xl font-serif mb-6 leading-tight">Privacy-First by Design</h2>
				<p class="text-gray-600 text-lg leading-relaxed">
					All transcription happens locally on your device. No audio is ever uploaded to the cloud. Your meetings stay yours.
				</p>
			</div>
			<div class="relative">
				<!-- Privacy graphic -->
				<div class="bg-white rounded-lg shadow-xl border border-gray-200 overflow-hidden transform rotate-1 p-8">
					<div class="flex items-center justify-center mb-6">
						<div class="relative">
							<div class="w-24 h-24 rounded-full border-4 border-gray-900 flex items-center justify-center">
								<svg class="w-12 h-12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
									<path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"/>
									<path d="M9 12l2 2 4-4"/>
								</svg>
							</div>
							<div class="absolute -right-2 -top-2 w-8 h-8 bg-green-500 rounded-full flex items-center justify-center">
								<svg class="w-5 h-5 text-white" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="3">
									<path d="M5 13l4 4L19 7"/>
								</svg>
							</div>
						</div>
					</div>
					<div class="space-y-3 text-sm">
						<div class="flex items-center gap-3 text-gray-700">
							<div class="w-2 h-2 rounded-full bg-green-500"></div>
							<span>On-device processing</span>
						</div>
						<div class="flex items-center gap-3 text-gray-700">
							<div class="w-2 h-2 rounded-full bg-green-500"></div>
							<span>Zero cloud uploads</span>
						</div>
						<div class="flex items-center gap-3 text-gray-700">
							<div class="w-2 h-2 rounded-full bg-green-500"></div>
							<span>No meeting bots</span>
						</div>
						<div class="flex items-center gap-3 text-gray-700">
							<div class="w-2 h-2 rounded-full bg-green-500"></div>
							<span>Complete data control</span>
						</div>
					</div>
				</div>
			</div>
		</div>
	</section>

	<!-- Grid Section -->
	<section class="bg-white text-dark-bg pb-24">
		<div class="max-w-6xl mx-auto px-6 grid md:grid-cols-2 gap-8">
			<!-- Card 1 -->
			<div class="bg-gray-50 rounded-2xl p-8 md:p-12">
				<h3 class="text-2xl font-serif mb-4">AI That Runs on Your Device</h3>
				<p class="text-gray-600 mb-8 text-sm leading-relaxed">
					State-of-the-art speech recognition models optimized for meeting contexts. Fast, accurate transcription without internet connectivity or cloud dependencies.
				</p>
				<div class="bg-white rounded-lg shadow-sm border border-gray-200 p-8 h-48 flex items-center justify-center relative overflow-hidden">
					<!-- Device icon -->
					<div class="relative">
						<div class="w-32 h-24 border-4 border-gray-900 rounded-lg flex items-center justify-center">
							<div class="text-center">
								<div class="w-12 h-12 bg-gray-900 rounded-full mx-auto mb-2 flex items-center justify-center">
									<svg class="w-6 h-6 text-white" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
										<circle cx="12" cy="12" r="3"/>
										<path d="M12 1v6m0 6v6M1 12h6m6 0h6"/>
									</svg>
								</div>
								<div class="text-[8px] font-semibold text-gray-500">LOCAL AI</div>
							</div>
						</div>
						<div class="absolute -right-3 -top-3 w-8 h-8 bg-green-500 rounded-full animate-pulse"></div>
					</div>
					<!-- Floating labels -->
					<div class="absolute top-4 left-4 bg-white shadow-md rounded px-2 py-1 text-[8px] border border-gray-100 text-gray-400">No internet needed</div>
					<div class="absolute bottom-4 right-4 bg-white shadow-md rounded px-2 py-1 text-[8px] border border-gray-100 text-gray-400">100% private</div>
				</div>
			</div>
			<!-- Card 2 -->
			<div class="bg-gray-50 rounded-2xl p-8 md:p-12">
				<h3 class="text-2xl font-serif mb-4">Handwritten + Transcribed Notes</h3>
				<p class="text-gray-600 mb-8 text-sm leading-relaxed">
					Hyprnote uniquely combines AI transcription with your handwritten notes, creating comprehensive meeting documentation that captures both spoken words and your insights.
				</p>
				<div class="bg-white rounded-lg shadow-sm border border-gray-200 p-6 h-48 flex items-center justify-center relative">
					<!-- Notes visualization -->
					<div class="w-full space-y-3">
						<div class="flex items-center gap-3">
							<div class="w-8 h-8 bg-gray-900 rounded flex items-center justify-center text-white text-xs font-bold">AI</div>
							<div class="flex-1 h-2 bg-gray-100 rounded"></div>
						</div>
						<div class="flex items-center gap-3">
							<div class="w-8 h-8 bg-gray-200 rounded flex items-center justify-center">
								<svg class="w-4 h-4" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
									<path d="M17 3a2.828 2.828 0 1 1 4 4L7.5 20.5 2 22l1.5-5.5L17 3z"/>
								</svg>
							</div>
							<div class="flex-1 h-2 bg-gray-100 rounded"></div>
						</div>
						<div class="flex items-center gap-3">
							<div class="w-8 h-8 bg-gray-900 rounded flex items-center justify-center text-white text-xs font-bold">AI</div>
							<div class="flex-1 h-2 bg-gray-100 rounded"></div>
						</div>
						<div class="flex items-center gap-3">
							<div class="w-8 h-8 bg-gray-200 rounded flex items-center justify-center">
								<svg class="w-4 h-4" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
									<path d="M17 3a2.828 2.828 0 1 1 4 4L7.5 20.5 2 22l1.5-5.5L17 3z"/>
								</svg>
							</div>
							<div class="flex-1 h-2 bg-gray-100 rounded"></div>
						</div>
					</div>
				</div>
			</div>
		</div>
	</section>

	<!-- Testimonial -->
	<section class="bg-dark-bg text-white py-32 relative overflow-hidden">
		<div class="max-w-4xl mx-auto px-6 text-center relative z-10">
			<div class="text-brand-primary-light text-6xl font-serif absolute -top-10 left-0 opacity-50">“</div>
			<blockquote class="text-3xl md:text-4xl font-serif leading-tight mb-12 relative">
				<span class="text-brand-primary-light absolute -left-4 -top-4">“</span>
				Finally, a meeting notes solution I can actually use. No more worrying about compliance violations or intrusive bots in client calls.
				<span class="text-brand-primary-light absolute -right-4 bottom-4">”</span>
			</blockquote>
			<div class="flex items-center justify-between border-t border-white/10 pt-8">
				<div class="text-sm font-mono tracking-wide uppercase text-gray-400">Healthcare Compliance Officer</div>
				<div class="flex gap-2">
					<button class="w-8 h-8 border border-white/20 flex items-center justify-center hover:bg-white/10 transition-colors">
						<svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M15 18l-6-6 6-6"/></svg>
					</button>
					<button class="w-8 h-8 border border-white/20 flex items-center justify-center hover:bg-white/10 transition-colors">
						<svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M9 18l6-6-6-6"/></svg>
					</button>
				</div>
			</div>
		</div>
	</section>

	<!-- Features Grid -->
	<section id="features" class="bg-white text-dark-bg py-24">
		<div class="text-center mb-16">
			<div class="text-[10px] uppercase tracking-widest text-gray-500 mb-4">+FEATURES</div>
			<h2 class="text-5xl md:text-6xl font-serif mb-4">
				Built for <br />
				Privacy-Conscious Professionals
			</h2>
			<p class="text-gray-600 mb-6">Essential capabilities for secure meeting documentation</p>
		</div>

		<!-- Feature Nav (Visual only based on screenshot) -->
		<div class="flex flex-wrap justify-center gap-6 text-sm text-gray-400 mb-16 border-b border-gray-100 pb-4 max-w-6xl mx-auto px-6">
			<span>Local Transcription</span>
			<span>Handwritten Notes</span>
			<span>Speaker Detection</span>
			<span class="text-black font-medium border-b-2 border-black pb-4 -mb-4.5">Smart Summaries</span>
			<span>Search & Export</span>
			<span>Calendar Sync</span>
			<span>Offline Mode</span>
		</div>

		<div class="max-w-6xl mx-auto px-6 space-y-8">
			<!-- Row 1: Real-time Transcription -->
			<div class="bg-gray-50 rounded-2xl p-8 md:p-12 grid md:grid-cols-2 gap-12 items-center">
				<div>
					<h3 class="text-2xl font-serif mb-4">Real-Time Local Transcription</h3>
					<p class="text-gray-600 text-sm leading-relaxed">
						Accurate speech-to-text transcription that happens entirely on your device. No delays, no internet required, no privacy concerns.
					</p>
				</div>
				<div class="bg-white shadow-lg shadow-gray-200/50 border border-gray-200 rounded-lg p-6 transform rotate-1 transition-transform hover:rotate-0">
					<div class="flex items-center gap-2 mb-4 text-xs text-gray-500">
						<div class="w-2 h-2 rounded-full bg-green-500 animate-pulse"></div>
						<span>Transcribing locally...</span>
					</div>
					<!-- Transcript preview -->
					<div class="space-y-3 text-xs">
						<div class="flex gap-2">
							<span class="font-semibold text-gray-700 min-w-[50px]">Sarah:</span>
							<span class="text-gray-600">Let's discuss the Q4 roadmap and key deliverables...</span>
						</div>
						<div class="flex gap-2">
							<span class="font-semibold text-gray-700 min-w-[50px]">Mike:</span>
							<span class="text-gray-600">I think we should prioritize the security audit first.</span>
						</div>
						<div class="flex gap-2 opacity-70">
							<span class="font-semibold text-gray-700 min-w-[50px]">Sarah:</span>
							<span class="text-gray-600">Agreed. Let's allocate two weeks for that...</span>
						</div>
					</div>
					<div class="mt-4 pt-3 border-t border-gray-100 flex items-center justify-between text-[10px] text-gray-400">
						<span>3 speakers detected</span>
						<span>Processing: 0ms latency</span>
					</div>
				</div>
			</div>

			<!-- Row 2: Smart Summaries & Speaker Detection -->
			<div class="grid md:grid-cols-2 gap-8">
				<div class="bg-gray-50 rounded-2xl p-8 md:p-12 relative overflow-hidden">
					<div class="relative z-10">
						<div class="bg-white rounded-lg shadow-sm border border-gray-200 p-4 mb-6">
							<div class="text-[10px] font-semibold text-gray-500 mb-2 uppercase">AI Summary</div>
							<div class="space-y-2 text-xs text-gray-700">
								<p class="font-medium">Key Decisions:</p>
								<ul class="space-y-1 ml-3">
									<li class="flex gap-2"><span>•</span><span>Security audit prioritized for Q4</span></li>
									<li class="flex gap-2"><span>•</span><span>Budget approved: $50K</span></li>
									<li class="flex gap-2"><span>•</span><span>Launch delayed to Jan 15</span></li>
								</ul>
							</div>
						</div>
						<h3 class="text-2xl font-serif mb-2">Smart Summaries</h3>
						<p class="text-gray-600 text-xs">AI-generated meeting summaries with key decisions and action items</p>
					</div>
				</div>
				<div class="bg-gray-50 rounded-2xl p-8 md:p-12">
					<div class="bg-white rounded-lg shadow-sm border border-gray-200 p-4 mb-8 max-w-xs mx-auto">
						<div class="text-xs font-semibold mb-3 border-b border-gray-100 pb-2">Speakers</div>
						<div class="space-y-2">
							<div class="flex items-center justify-between text-xs">
								<div class="flex items-center gap-2">
									<div class="w-6 h-6 bg-blue-100 rounded-full flex items-center justify-center text-blue-600 text-[10px] font-bold">S</div>
									<span class="font-medium">Sarah Chen</span>
								</div>
								<span class="text-gray-400">42%</span>
							</div>
							<div class="flex items-center justify-between text-xs">
								<div class="flex items-center gap-2">
									<div class="w-6 h-6 bg-green-100 rounded-full flex items-center justify-center text-green-600 text-[10px] font-bold">M</div>
									<span class="font-medium">Mike Torres</span>
								</div>
								<span class="text-gray-400">35%</span>
							</div>
							<div class="flex items-center justify-between text-xs">
								<div class="flex items-center gap-2">
									<div class="w-6 h-6 bg-purple-100 rounded-full flex items-center justify-center text-purple-600 text-[10px] font-bold">A</div>
									<span class="font-medium">Alex Kim</span>
								</div>
								<span class="text-gray-400">23%</span>
							</div>
						</div>
					</div>
					<h3 class="text-2xl font-serif mb-2">Speaker Detection</h3>
					<p class="text-gray-600 text-xs">Automatically identify and label different speakers in your meetings</p>
				</div>
			</div>

			<!-- Row 3: Search & Export -->
			<div class="bg-gray-50 rounded-2xl p-8 md:p-12 grid md:grid-cols-2 gap-12 items-center">
				<div>
					<h3 class="text-2xl font-serif mb-4">Powerful Search & Export</h3>
					<p class="text-gray-600 text-sm leading-relaxed mb-6">
						Search across all your meeting notes instantly. Export to PDF, Markdown, or your favorite note-taking app.
					</p>
					<div class="space-y-2 text-xs text-gray-500">
						<div class="flex items-center gap-2 border-b border-gray-200 pb-2">
							<svg class="w-3 h-3" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="11" cy="11" r="8"/><path d="m21 21-4.35-4.35"/></svg>
							<span>Full-text search</span>
						</div>
						<div class="flex items-center gap-2 border-b border-gray-200 pb-2">
							<svg class="w-3 h-3" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M21 15v4a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2v-4"/><polyline points="7 10 12 15 17 10"/><line x1="12" y1="15" x2="12" y2="3"/></svg>
							<span>Export to PDF, Markdown, TXT</span>
						</div>
					</div>
				</div>
				<div class="relative h-48 flex items-center justify-center">
					<div class="bg-white rounded-lg shadow-lg border border-gray-200 p-4 w-full max-w-xs">
						<div class="flex items-center gap-2 bg-gray-50 rounded px-3 py-2 mb-3">
							<svg class="w-4 h-4 text-gray-400" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="11" cy="11" r="8"/><path d="m21 21-4.35-4.35"/></svg>
							<input type="text" placeholder="Search meetings..." class="bg-transparent text-xs flex-1 outline-none" />
						</div>
						<div class="space-y-2 text-xs">
							<div class="p-2 bg-yellow-50 border border-yellow-100 rounded">
								<div class="font-medium">Q4 Strategy</div>
								<div class="text-gray-500 text-[10px]">...approved budget of $50K...</div>
							</div>
							<div class="p-2 hover:bg-gray-50 rounded">
								<div class="font-medium">Client Sync</div>
								<div class="text-gray-500 text-[10px]">...compliance requirements...</div>
							</div>
						</div>
					</div>
				</div>
			</div>

			<!-- Row 4: 3 Cards -->
			<div class="grid md:grid-cols-3 gap-8">
				<div class="bg-gray-50 rounded-2xl p-8">
					<div class="bg-white border border-gray-200 rounded p-4 mb-6 shadow-sm">
						<div class="flex items-center gap-2 mb-2">
							<svg class="w-4 h-4 text-gray-700" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
								<path d="M18 8A6 6 0 0 0 6 8c0 7-3 9-3 9h18s-3-2-3-9"/>
								<path d="M13.73 21a2 2 0 0 1-3.46 0"/>
							</svg>
							<span class="text-xs font-semibold">Meeting in 5 min</span>
						</div>
						<div class="text-[10px] text-gray-500">
							Q4 Planning • 2:00 PM
						</div>
					</div>
					<h3 class="text-xl font-serif mb-2">Calendar Integration</h3>
					<p class="text-gray-500 text-xs">Sync with your calendar to automatically organize and prepare for meetings</p>
				</div>
				<div class="bg-gray-50 rounded-2xl p-8">
					<div class="bg-white border border-gray-200 rounded p-3 mb-6 shadow-sm">
						<div class="flex items-center justify-between mb-2">
							<span class="text-xs font-medium">Offline Mode</span>
							<div class="w-8 h-4 bg-green-500 rounded-full relative">
								<div class="absolute right-0.5 top-0.5 w-3 h-3 bg-white rounded-full"></div>
							</div>
						</div>
						<div class="text-[10px] text-gray-400">Works without internet</div>
					</div>
					<h3 class="text-xl font-serif mb-2">Offline First</h3>
					<p class="text-gray-500 text-xs">Full functionality without internet connection - perfect for secure environments</p>
				</div>
				<div class="bg-gray-50 rounded-2xl p-8">
					<div class="bg-white border border-gray-200 rounded p-4 mb-6 shadow-sm">
						<div class="flex items-center gap-2 mb-2">
							<svg class="w-4 h-4 text-gray-700" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
								<path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"/>
							</svg>
							<span class="text-xs font-semibold">Data stays local</span>
						</div>
						<div class="text-[10px] text-gray-500">
							Zero cloud storage
						</div>
					</div>
					<h3 class="text-xl font-serif mb-2">Your Data, Your Device</h3>
					<p class="text-gray-500 text-xs">Complete control over your meeting data with no cloud dependencies</p>
				</div>
			</div>

			<!-- Row 5: 2 Cards -->
			<div class="grid md:grid-cols-2 gap-8">
				<div class="bg-gray-50 rounded-2xl p-8 flex flex-col justify-between">
					<div class="bg-white border border-gray-200 rounded-lg p-4 shadow-sm mb-8">
						<div class="flex items-center gap-2 mb-3">
							<svg class="w-4 h-4 text-gray-700" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
								<path d="M17 3a2.828 2.828 0 1 1 4 4L7.5 20.5 2 22l1.5-5.5L17 3z"/>
							</svg>
							<span class="text-xs font-semibold">Handwritten Notes</span>
						</div>
						<div class="space-y-1 text-[10px] text-gray-500">
							<div>• Action items from discussion</div>
							<div>• Personal insights & observations</div>
							<div>• Follow-up questions</div>
						</div>
					</div>
					<div>
						<h3 class="text-xl font-serif mb-2">Combine with Your Notes</h3>
						<p class="text-gray-500 text-xs">Add your own notes alongside AI transcription for complete context</p>
					</div>
				</div>
				<div class="bg-gray-50 rounded-2xl p-8">
					<div class="bg-white border border-gray-200 rounded-lg p-4 mb-6 shadow-sm">
						<div class="flex items-center justify-between mb-3">
							<span class="text-xs font-semibold">Multi-language Support</span>
							<span class="text-[10px] text-gray-500">20+ languages</span>
						</div>
						<div class="flex flex-wrap gap-1">
							<span class="text-[10px] bg-gray-100 px-2 py-1 rounded">English</span>
							<span class="text-[10px] bg-gray-100 px-2 py-1 rounded">Spanish</span>
							<span class="text-[10px] bg-gray-100 px-2 py-1 rounded">French</span>
							<span class="text-[10px] bg-gray-100 px-2 py-1 rounded">German</span>
							<span class="text-[10px] bg-gray-100 px-2 py-1 rounded">Japanese</span>
							<span class="text-[10px] bg-gray-100 px-2 py-1 rounded">+15 more</span>
						</div>
					</div>
					<h3 class="text-xl font-serif mb-2">Global Language Support</h3>
					<p class="text-gray-500 text-xs">Transcribe meetings in 20+ languages with high accuracy</p>
				</div>
			</div>
		</div>
	</section>

	<!-- Data Sources -->
	<section class="bg-dark-bg text-white py-24 border-t border-white/5">
		<div class="max-w-4xl mx-auto px-6 text-center">
			<div class="text-[10px] uppercase tracking-widest text-gray-500 mb-4">\+INTEGRATIONS</div>
			<h2 class="text-3xl md:text-5xl font-serif mb-6">Works with your favorite tools</h2>
			<p class="text-gray-400 mb-12">Export and sync your meeting notes seamlessly</p>

			<div class="bg-[#0A1F1E] border border-white/10 rounded-xl overflow-hidden max-w-md mx-auto relative">
				<div class="p-4 flex items-center gap-4 border-b border-white/5 bg-[#0F2928] relative z-10">
					<div class="w-8 h-8 bg-white rounded flex items-center justify-center shadow-lg shadow-brand-green/20">
						<div class="w-4 h-4 bg-black grid grid-cols-2 gap-0.5"><div class="bg-white"></div><div class="bg-white"></div><div class="bg-white"></div><div class="bg-white"></div></div>
					</div>
					<div class="text-left">
						<div class="text-sm font-medium text-white">Hyprnote</div>
						<div class="text-[10px] text-brand-primary-light flex items-center gap-1">
							<span class="w-1 h-1 bg-brand-green rounded-full animate-pulse"></span>
							Accessing data sources...
						</div>
					</div>
				</div>
				
				<!-- Connecting line visual -->
				<div class="absolute left-8 top-12 bottom-0 w-px bg-gradient-to-b from-white/20 to-transparent z-0"></div>

				<div class="divide-y divide-white/5 text-sm text-gray-400 text-left relative z-10">
					<div class="p-4 pl-16 hover:bg-white/5 transition-colors cursor-pointer flex items-center justify-between group">
						<span>Notion</span>
						<span class="opacity-0 group-hover:opacity-100 text-xs text-brand-primary-light">Connected</span>
					</div>
					<div class="p-4 pl-16 hover:bg-white/5 transition-colors cursor-pointer flex items-center justify-between group">
						<span>Google Calendar</span>
						<span class="opacity-0 group-hover:opacity-100 text-xs text-brand-primary-light">Connected</span>
					</div>
					<div class="p-4 pl-16 hover:bg-white/5 transition-colors cursor-pointer flex items-center justify-between group">
						<span>Obsidian</span>
						<span class="opacity-0 group-hover:opacity-100 text-xs text-brand-primary-light">Connected</span>
					</div>
				</div>
			</div>
		</div>
	</section>

	<!-- Security -->
	<section id="security" class="bg-white text-dark-bg py-24">
		<div class="max-w-6xl mx-auto px-6 grid md:grid-cols-2 gap-16">
			<div>
				<div class="text-[10px] uppercase tracking-widest text-gray-500 mb-4">+SECURITY</div>
				<h2 class="text-4xl md:text-5xl font-serif mb-6">Enterprise-grade security</h2>
				<p class="text-gray-600 mb-8 leading-relaxed">
					Your data is encrypted both in transit and at rest, utilizing the most robust encryption standards: AES-256 for storage and TLS 1.2/1.3 for secure communication
				</p>
				<a href="#" class="inline-flex items-center gap-2 font-medium hover:underline">
					<div class="w-5 h-5 bg-black text-white flex items-center justify-center rounded-sm text-xs">→</div>
					Learn more
				</a>
			</div>
			<div class="grid grid-cols-2 gap-px bg-gray-200 border border-gray-200">
				<!-- SOC 2 -->
				<div class="bg-white p-8 flex items-center justify-center aspect-square">
					<div class="w-24 h-24 rounded-full border-2 border-black flex flex-col items-center justify-center relative p-2">
						<div class="absolute inset-1 border border-black rounded-full"></div>
						<div class="text-[8px] uppercase tracking-widest font-semibold mb-1">AICPA</div>
						<div class="text-lg font-bold leading-none">SOC</div>
						<div class="text-[10px] font-bold">2</div>
					</div>
				</div>
				<!-- ISO -->
				<div class="bg-white p-8 flex items-center justify-center aspect-square">
					<div class="w-24 h-24 rounded-full border-2 border-black flex flex-col items-center justify-center relative p-2">
						<div class="absolute inset-1 border border-dashed border-black rounded-full"></div>
						<div class="text-xl font-bold">ISO</div>
						<div class="text-[10px] font-bold bg-black text-white px-1 rounded-sm mt-1">27001</div>
					</div>
				</div>
				<!-- CCPA -->
				<div class="bg-white p-8 flex items-center justify-center aspect-square">
					<div class="w-24 h-24 rounded-full border border-black flex flex-col items-center justify-center relative p-2">
						<div class="text-lg font-serif">CCPA</div>
						<div class="text-[8px] uppercase tracking-widest mt-1">Ready</div>
					</div>
				</div>
				<!-- GDPR -->
				<div class="bg-white p-8 flex items-center justify-center aspect-square">
					<div class="w-24 h-24 rounded-full border border-dashed border-black flex flex-col items-center justify-center relative p-2">
						<div class="absolute top-2 text-[10px]">* * *</div>
						<div class="text-lg font-bold">GDPR</div>
						<div class="absolute bottom-2 text-[10px]">* * *</div>
					</div>
				</div>
			</div>
		</div>
	</section>

	<!-- FAQs -->
	<section class="bg-white text-dark-bg pb-32">
		<div class="max-w-3xl mx-auto px-6">
			<div class="text-[10px] uppercase tracking-widest text-gray-500 mb-4">+FAQS</div>
			<h2 class="text-4xl md:text-5xl font-serif mb-12">FAQs</h2>

			<div class="border-t border-gray-200">
				{#each faqs as faq}
					<details class="group border-b border-gray-200">
						<summary class="flex justify-between items-center py-6 cursor-pointer list-none">
							<span class="font-medium text-lg pr-8">{faq.question}</span>
							<span class="transition group-open:rotate-45">
								<svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1"><path d="M12 5v14M5 12h14"/></svg>
							</span>
						</summary>
						<div class="text-gray-600 pb-6 leading-relaxed">
							{faq.answer}
						</div>
					</details>
				{/each}
			</div>
		</div>
	</section>

	<!-- CTA Footer -->
	<section class="bg-dark-bg text-white py-32 relative overflow-hidden">
		<!-- Grid Background Effect -->
		<div class="absolute inset-0 opacity-20 pointer-events-none" 
			 style="background-image: linear-gradient(rgba(255,255,255,0.05) 1px, transparent 1px), linear-gradient(90deg, rgba(255,255,255,0.05) 1px, transparent 1px); background-size: 50px 50px;">
		</div>
		<div class="absolute bottom-0 left-0 right-0 h-64 bg-gradient-to-t from-brand-green/20 to-transparent pointer-events-none"></div>

		<div class="max-w-4xl mx-auto px-6 relative z-10">
			<div class="text-[10px] uppercase tracking-widest text-brand-primary-light mb-4">+GET STARTED</div>
			<h2 class="text-5xl md:text-7xl font-serif mb-12 leading-tight">
				Take control of your meeting notes
			</h2>
			<div class="flex flex-wrap gap-4">
				<button class="bg-white text-dark-bg px-6 py-3 rounded font-medium hover:bg-gray-100 transition-colors">
					Enterprise access
				</button>
				<button class="bg-white text-dark-bg px-6 py-3 rounded font-medium hover:bg-gray-100 transition-colors">
					Join Waitlist
				</button>
			</div>
		</div>
	</section>

	<!-- Footer -->
	<footer class="bg-[#030e0e] text-gray-400 py-12 border-t border-white/5 relative overflow-hidden">
		<div class="max-w-7xl mx-auto px-6 relative z-10">
			<div class="grid grid-cols-2 md:grid-cols-4 gap-8 mb-24 text-sm">
				<div>
					<h4 class="text-white font-semibold mb-4">Product</h4>
				</div>
				<div></div>
				<div></div>
				<div class="text-right">
					<h4 class="text-white font-semibold mb-4">Security</h4>
				</div>
				<div>
					<h4 class="text-white font-semibold mb-4">Legal</h4>
				</div>
				<div class="col-span-3 text-right">
					<div class="space-x-4">
						<a href="#" class="hover:text-white">Privacy</a>
						<span>/</span>
						<a href="#" class="hover:text-white">Terms</a>
						<span>/</span>
						<a href="#" class="hover:text-white">End User License Agreement</a>
					</div>
				</div>
			</div>

			<div class="flex justify-between items-end border-t border-white/5 pt-8">
				<div class="flex items-center gap-4">
					<span class="text-white font-serif text-xl">Hyprnote</span>
					<span class="text-xs text-gray-600">Hyprnote 2025. All Rights Reserved</span>
				</div>
				<div class="flex items-center gap-4 text-xs">
					<a href="#" class="hover:text-white">LinkedIn</a>
					<span>/</span>
					<a href="#" class="hover:text-white">X</a>
				</div>
			</div>
		</div>

		<!-- Big Watermark -->
		<div class="absolute bottom-0 left-0 right-0 flex justify-center pointer-events-none overflow-hidden">
			<div class="text-[20vw] font-serif text-white/5 leading-none -mb-10 select-none">
				Hyprnote
			</div>
		</div>
	</footer>
</div>

<style>
	/* Custom scrollbar for details/summary if needed, but default is fine */
	details > summary {
		list-style: none;
	}
	details > summary::-webkit-details-marker {
		display: none;
	}
</style>

