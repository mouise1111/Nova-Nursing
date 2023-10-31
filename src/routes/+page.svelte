<script>
	import gsap from 'gsap';
	import { ScrollTrigger } from 'gsap/dist/ScrollTrigger';
	import { onMount } from 'svelte';
	import Navbar from '../components/Navbar.svelte';
	import Services from '../components/Services.svelte';
	function scrollIntoView({ target }) {
		const el = document.querySelector(target.getAttribute('href'));
		if (!el) return;
		el.scrollIntoView({
			behavior: 'smooth'
		});
	}
	onMount(() => {
		gsap.registerPlugin(ScrollTrigger);

		let tl = gsap.timeline();

		// Team
		gsap.fromTo(
			'.team-picture ',
			{ x: -100, opacity: 0 },
			{
				opacity: 1,
				x: 0,
				duration: 1,
				// delay: 0.5,
				scrollTrigger: {
					trigger: '.third-screen',
					start: 'top center'
					// end: 'bottom 20%',
					// scrub: true
				}
			}
		);
		gsap.fromTo(
			'.team-container',
			{ x: 100, opacity: 0 },
			{
				opacity: 1,
				x: 0,
				duration: 1,
				// delay: 0.5,
				scrollTrigger: {
					trigger: '.second-screen',
					start: 'top top'
					// end: 'bottom 20%',
					// scrub: true
				}
			}
		);

		// Diensten
		gsap.fromTo(
			'.title-diensten',
			{ opacity: 0 },
			{
				opacity: 1,
				x: 0,
				duration: 1,
				// delay: 0.5,
				scrollTrigger: {
					trigger: '.second-screen',
					start: 'top center'
					// end: 'bottom 20%',
					// scrub: true
				}
			}
		);
		gsap.fromTo(
			'.title-diensten-2',
			{ opacity: 0 },
			{
				opacity: 1,
				x: 0,
				duration: 1,
				delay: 0.5,
				scrollTrigger: {
					trigger: '.second-screen',
					start: 'top center'
					// end: 'bottom 20%',
					// scrub: true
				}
			}
		);
		gsap.fromTo(
			'.container-diensten',
			{ opacity: 0, y: 100 },
			{
				opacity: 1,
				y: 0,
				duration: 1,
				delay: 0.5,
				scrollTrigger: {
					trigger: '.second-screen',
					start: 'top center'
					// end: 'bottom 20%',
					// scrub: true
				}
			}
		); // Contact
		gsap.fromTo(
			'.contact-title1',
			{ opacity: 0 },
			{
				opacity: 1,
				x: 0,
				duration: 1,
				// delay: 0.5,
				scrollTrigger: {
					trigger: '.last-screen',
					start: 'top center'
					// end: 'bottom 20%',
					// scrub: true
				}
			}
		);
		gsap.fromTo(
			'.contact-title2',
			{ opacity: 0 },
			{
				opacity: 1,
				x: 0,
				duration: 1,
				delay: 0.5,
				scrollTrigger: {
					trigger: '.last-screen',
					start: 'top center'
					// end: 'bottom 20%',
					// scrub: true
				}
			}
		);
		gsap.fromTo(
			'.form-container',
			{ opacity: 0, x: 100 },
			{
				opacity: 1,
				x: 0,
				duration: 1,
				delay: 1,
				scrollTrigger: {
					trigger: '.last-screen',
					start: 'top center'
					// end: 'bottom 20%',
					// scrub: true
				}
			}
		);
		gsap.fromTo(
			'.contact-container',
			{ opacity: 0, x: -100 },
			{
				opacity: 1,
				x: 0,
				duration: 1,
				delay: 1,
				scrollTrigger: {
					trigger: '.last-screen',
					start: 'top center'
					// end: 'bottom 20%',
					// scrub: true
				}
			}
		);

		// Review

		// Diensten
		gsap.fromTo(
			'.title-review',
			{ opacity: 0 },
			{
				opacity: 1,
				x: 0,
				duration: 1,
				// delay: 0.5,
				scrollTrigger: {
					trigger: '.fourth-screen',
					start: 'top center'

					// end: 'bottom 20%',
					// scrub: true
				}
			}
		);

		gsap.fromTo(
			'.title-review',
			{ opacity: 0 },
			{
				opacity: 1,
				x: 0,
				duration: 1,
				// delay: 0.5,
				scrollTrigger: {
					trigger: '.fourth-screen',
					start: 'top center'

					// end: 'bottom 20%',
					// scrub: true
				}
			}
		);
		// gsap.fromTo(
		// 	'.counter',
		// 	{ opacity: 0, x: 200 },
		// 	{
		// 		opacity: 1,
		// 		x: 0,
		// 		duration: 3,
		// 		increase,
		// 		// delay: 0.5,
		// 		scrollTrigger: {
		// 			trigger: '.fourth-screen',
		// 			start: 'top center'

		// 			// end: 'bottom 20%',
		// 			// scrub: true
		// 		}
		// 	}
		// );
		gsap.fromTo(
			'.container-review',
			{ opacity: 0, y: 100 },
			{
				opacity: 1,
				y: 0,
				duration: 1,
				delay: 0.4,
				scrollTrigger: {
					trigger: '.fourth-screen',
					start: 'top center'
					// snap: {
					// 	snapTo: 1, // Adjust this value to control the snap position (e.g., 0.5 means halfway through the scroll)
					// 	duration: 1 // Adjust this value to control the snap animation duration
					// }
					// end: 'bottom 20%',
					// scrub: true
				}
			}
		);
		tl.addLabel('start')
			.from('.title-1', { x: 100, opacity: 0, ease: 'power', duration: 0.3 })
			.from('.title-2', { x: 100, opacity: 0, ease: 'power', duration: 0.3 })
			.from('.paragraph-1', { x: 100, opacity: 0, ease: 'power', duration: 0.3 })
			.from('.contact-btn', { x: -100, opacity: 0, ease: 'power' })
			.from('.doc ', { scale: 0, rotation: 45, autoAlpha: 0 });
	});
</script>

<Navbar />
<main class="lg:pt-20 md:pt-20 lg:px-24 sm:w-full">
	<div class=" lg:h-screen first-screen md:mb-16 lg:mb-0" id="home">
		<div class="pt-5 lg:pt-16">
			<!-- <h1 class="my-3 text-6xl font-extrabold tracking-wider sm:text-sm">
				Met een hart voor <span class="text-lime-600">Zorg</span>
			</h1> -->
			<h1
				class="mx-2 my-3 text-5xl font-extrabold tracking-wider md:text-5xl lg:text-6xl lg:mx-0 title-1"
			>
				Met een hart voor <span class="text-lime-600">Zorg</span>
			</h1>

			<h2
				class="mx-2 my-5 text-4xl font-bold tracking-wider text-right lg:mx-0 lg:text-left title-2"
			>
				Thuisverpleging
			</h2>
			<p class="mx-2 my-3 lg:text-lg text-md lg:w-1/2 lg:mx-0 paragraph-1">
				Welkom bij Nova - Uw vertrouwde partner voor thuisverpleging. Onze toegewijde en ervaren
				verpleegkundigen bieden gepersonaliseerde zorg en ondersteuning in de comfortabele omgeving
				van uw eigen huis.<br /> Wij bedienen met trots de gemeente
				<span class="font-semibold">Sint-Pieters-Leeuw</span>
				en zijn specifiek actief in de gebieden <span class="font-semibold">Zuun</span>,
				<span class="font-semibold">Negenmanneke</span>, <span class="font-semibold">Rink</span> en
				<span class="font-semibold">Oudenaken</span>.
			</p>
			<button
				class="px-5 py-3 mx-2 my-3 text-white rounded-lg bg-lime-600 hover:bg-lime-500 contact-btn lg:mx-0"
			>
				<a href="#contact" on:click|preventDefault={scrollIntoView}>Contacteer ons</a>
			</button>
		</div>
		<img
			src="/female_doctor_2.png"
			alt=""
			class="absolute bottom-0 right-0 z-10 hidden mt-12 lg:w-1/2 doc lg:block"
		/>
		<img
			src="/ellipse1.png"
			alt="ellipse"
			class="absolute bottom-0 right-0 hidden lg:w-1/2 ellilpse lg:block"
		/>
	</div>
	<Services />
	<div
		id="team"
		class="flex items-center mb-0 text-center lg:h-screen lg:text-left third-screen lg:pt-0 md:mb-16 lg:mb-0"
	>
		<div class="flex-row items-center justify-between rounded lg:flex lg:content-center">
			<div class="flex justify-center order-last lg:w-1/2 lg:order-first">
				<img
					src="/Nurses-Day.jpg"
					alt="team"
					class="hidden w-4/5 rounded-3xl team-picture lg:block"
				/>
			</div>
			<div class="p-2 lg:w-1/2 lg:p-5 team-container">
				<h3 class=" bold text-lime-600">Tot uw dienst</h3>
				<h2 class="my-4 text-2xl">Maak kennis met ons zorgzame team</h2>
				<!-- <p class="mx-2 my-3 text-md lg:w-1/2 lg:mx-0"></p> -->
				<p class="text-md">
					Ons toegewijde team staat volledig tot uw dienst om hoogwaardige zorg te bieden. We
					begrijpen dat uw welzijn van het grootste belang is en streven ernaar om u de beste
					zorgervaring te bieden. Met een team van ervaren professionals zijn we uitgerust om aan al
					uw zorgbehoeften te voldoen.
				</p>
				<div class="flex justify-center mt-5 flew-row lg:justify-start">
					<img src="/check-icon.png" alt="" />
					<p class="px-3 font-medium bold text-md">Experten</p>
				</div>
				<div class="flex justify-center mt-3 flew-row lg:justify-start">
					<img src="/check-icon.png" alt="" />
					<p class="px-3 font-medium bold text-md">+20 jaar ervaring</p>
				</div>
			</div>

			<div class="flex justify-center order-last mx-auto mt-4 lg:hidden">
				<img
					src="/Nurses-Day.jpg"
					alt="team"
					class="block p-3 rounded-3xl team-picture md:w-4/5 lg:hidden"
				/>
			</div>
		</div>
	</div>
	<div
		id="review"
		class="mt-0 mb-0 md:mb-32 sm fourth-screen lg:mb-0 lg:h-screen lg:flex lg:flex-col lg:content-center lg:justify-center"
	>
		<h3 class="mt-16 text-center bold text-lime-600 lg:mt-0 title-review">Onze Beoordeling</h3>
		<!-- <h2 class="px-2 my-4 text-2xl text-center">
			Nova heeft een ruim zorgaanbod voor elke persoon die aangesloten is bij een Belgische
			mutualiteit.
		</h2> -->
		<div
			class="justify-center mx-auto lg:flex lg:flex-row lg:gap-8 lg:max-w-6xl lg:my-24 diensten lg:justify-between container-review"
		>
			<div
				class="flex flex-col justify-center h-56 gap-4 py-5 mx-auto my-8 text-center border-t-4 rounded-md shadow-lg border-lime-600 w-80 lg:w-80 md:w-64 lg:h-64 lg:py-10 lg:my-0 lg:text-left md:text-left"
			>
				<h3 class="py-2 text-4xl text-center lg:text-5xl">6</h3>
				<h4 class="text-center">Geverifieerde specialisten</h4>
			</div>
			<div
				class="flex flex-col justify-center h-56 gap-4 py-5 mx-auto my-8 text-center border-t-4 rounded-md shadow-lg border-lime-600 w-80 lg:w-80 md:w-64 lg:h-64 lg:py-10 lg:my-0 lg:text-left md:text-left"
			>
				<!-- <h3 class="py-2 text-4xl text-center lg:text-5xl" this:value={count} /> -->
				<h3 class="py-2 text-4xl text-center lg:text-5xl">+50</h3>
				<h4 class="text-center">Tevreden klanten</h4>
			</div>
			<div
				class="flex flex-col justify-center h-56 gap-4 py-5 mx-auto my-8 text-center border-t-4 rounded-md shadow-lg border-lime-600 w-80 lg:w-80 md:w-64 lg:h-64 lg:py-10 lg:my-0 lg:text-left md:text-left"
			>
				<h3 class="py-2 text-4xl text-center lg:text-5xl">99,7%</h3>
				<h4 class="text-center">Positieve feedback</h4>
			</div>
		</div>
	</div>
	<!-- <div
		id="contact"
		class="justify-center h-screen mb-0 md:mb-32 lg:mb-0 last-screen lg:flex lg:flex-col"
	>
		<h3 class="mt-16 font-bold text-center text-lime-600 lg:mt-0 contact-title1">Contacteer ons</h3>
		<h2 class="px-2 my-4 mb-8 text-2xl text-center lg:mb-16 contact-title2">
			Wenst u thuisverpleging aan te vragen, gebruik te maken van onze ondersteunende diensten of
			heeft u een vraag? Aarzel dan niet om ons te contacteren!
		</h2>
		<div class="flex flex-col lg:flex-row lg:justify-between sm:justify-center">
			<div
				class="flex flex-col items-center mb-8 lg:items-start lg:mb-0 lg:justify-center lg:min-w-fit lg:px-4 lg:ml-8 contact-container"
			>
				<div class="flex flex-row items-center justify-between mb-4">
					<img src="/phone-solid.svg" alt="" class="w-8 mx-2 lg:mx-0 lg:w-12 lg:mr-4" />
					<a href="tel:+31612345678">+0473 95 28 64</a>
				</div>

				<div class="flex flex-row items-center justify-between mb-4">
					<img src="/envelope-solid.svg" alt="" class="w-8 mx-2 lg:mx-0 lg:w-12 lg:mr-4" />

					<a href="mailto:lyhxr@example.com">info@norwich.edu</a>
				</div>
			</div>
			<div class="mx-2 lg:w-full form-container">
				<form
					action="https://formspree.io/f/xgejwpke"
					method="POST"
					class="max-w-lg mx-auto lg:max-w-4xl"
				>
					<div class="mb-4">
						<label for="name" class="block font-semibold text-gray-700">Naam</label>
						<input
							type="text"
							id="name"
							name="name"
							class="w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-lime-600"
							required
						/>
					</div>
					<div class="mb-4">
						<label for="email" class="block font-semibold text-gray-700">E-mailadres</label>
						<input
							type="email"
							id="email"
							name="email"
							class="w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-lime-600"
							required
						/>
					</div>
					<div class="mb-4">
						<label for="message" class="block font-semibold text-gray-700">Bericht</label>
						<textarea
							id="message"
							name="message"
							rows="4"
							class="w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-lime-600"
							required
						/>
					</div>
					<button
						type="submit"
						class="px-5 py-3 text-white rounded-lg bg-lime-600 hover:bg-lime-500 send-btn"
						>Verzenden</button
					>
				</form>
			</div>
		</div>
	</div> -->
	<div
		id="contact"
		class="flex flex-col content-center justify-center gap-4 mb-0 lg:mb-0 lg:h-screen last-screen lg:text-lg text-l"
	>
		<div>
			<h3 class="mt-16 font-bold text-center text-lime-600 lg:mt-0 contact-title1">
				Contacteer ons
			</h3>
			<h2 class="px-2 my-4 mb-8 text-2xl text-center lg:mb-16 contact-title2">
				Wenst u thuisverpleging aan te vragen, gebruik te maken van onze ondersteunende diensten of
				heeft u een vraag? Aarzel dan niet om ons te contacteren!
			</h2>
		</div>
		<div
			class="flex flex-col items-center content-center mb-8 lg:mb-0 lg:justify-center lg:min-w-fit lg:px-4 contact-container"
		>
			<div
				class="flex items-center justify-center w-12 h-12 mb-8 border-2 rounded-full border-lime-500 lg:w-20 lg:h-20"
			>
				<img src="/phone-solid.svg" alt="" class="w-12 m-4 lg:w-12" />
			</div>
			<div class="flex flex-row items-center justify-between gap-4 mb-4">
				<a href="tel:+32473952864" class="underline">0473 95 28 64</a>
				<h3>An De Ro</h3>
			</div>

			<div class="flex flex-row items-center justify-between gap-4 mb-4">
				<a href="tel:+32496569360" class="underline">0496 56 93 60</a>
				<h3>Vicky Van Biesen</h3>
			</div>

			<div class="flex flex-row items-center justify-between gap-4 mb-4">
				<a href="tel:+32473578230" class="underline">0473 57 82 30</a>
				<h3>Kelly van Cutsem</h3>
			</div>

			<div class="flex flex-row items-center justify-between gap-4 mb-4">
				<a href="tel:+32472450324" class="underline">0472 45 03 24</a>
				<h3>Yilke Read</h3>
			</div>
		</div>
	</div>
</main>
<footer class="py-4 mt-8 bg-gray-200 lg:mt-8">
	<div class="lg:px-24">
		<div class="flex flex-col items-center justify-center">
			<div class="flex flex-row gap-4">
				<a href="https://www.instagram.com/thuisverpleging_nova/" target="_blank" class="mb-2">
					<img src="/instagram.svg" alt="instagram icon" class="w-10" />
				</a><a href="https://www.facebook.com/ThuisverplegingNova" target="_blank" class="mb-2">
					<img src="/facebook.svg" alt="facebook icon" class="w-10" />
				</a>
			</div>
			<p class="text-gray-600">&copy; 2023 Nova. Alle rechten voorbehouden.</p>
		</div>
	</div>
</footer>

<style lang="postcss">
	:global(html) {
		background-color: theme(colors.gray.100);
		font-family: Manrope;
	}

	main {
		margin: 0;
		box-sizing: border-box;
		width: 100%;
		overflow: hidden;
	}

	.contact-btn {
		transition: background-color 0.3s ease;
	}
</style>
