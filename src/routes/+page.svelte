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
		// gsap.fromTo(
		// 	'.container-diensten',
		// 	{ opacity: 0, y: 100 },
		// 	{
		// 		opacity: 1,
		// 		y: 0,
		// 		duration: 1,
		// 		delay: 0.5,
		// 		scrollTrigger: {
		// 			trigger: '.second-screen',
		// 			start: 'top center'
		// 			// end: 'bottom 20%',
		// 			// scrub: true
		// 		}
		// 	}
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

<main class="lg:px-24 sm:w-full">
	<div class=" lg:h-screen first-screen md:mb-16 lg:mb-0">
		<Navbar />
		<div class="lg:pt-16 pt-5">
			<!-- <h1 class="text-6xl tracking-wider font-extrabold my-3 sm:text-sm">
				Met een hart voor <span class="text-lime-600">Zorg</span>
			</h1> -->
			<h1
				class="text-5xl md:text-5xl lg:text-6xl tracking-wider font-extrabold my-3 mx-2 lg:mx-0 title-1"
			>
				Met een hart voor <span class="text-lime-600">Zorg</span>
			</h1>

			<h2
				class="text-4xl font-bold tracking-wider my-5 mx-2 lg:mx-0 lg:text-left text-right title-2"
			>
				Thuisverpleging
			</h2>
			<p class="lg:text-lg text-md lg:w-1/2 my-3 mx-2 lg:mx-0 paragraph-1">
				Welkom bij Nova - Uw vertrouwde partner voor thuisverpleging. Onze toegewijde en ervaren
				verpleegkundigen bieden gepersonaliseerde zorg en ondersteuning in de comfortabele omgeving
				van uw eigen huis.<br /> Wij bedienen met trots de gemeente
				<span class="font-semibold">Sint-Pieters-Leeuw</span>
				en zijn specifiek actief in de gebieden <span class="font-semibold">Zuun</span>,
				<span class="font-semibold">Negenmanneke</span>, <span class="font-semibold">Rink</span> en
				<span class="font-semibold">Oudenaken</span>.
			</p>
			<button
				class="py-3 px-5 bg-lime-600 hover:bg-lime-500 text-white rounded-lg my-3 contact-btn mx-2 lg:mx-0"
			>
				<a href="#contact" on:click|preventDefault={scrollIntoView}>Contacteer ons</a>
			</button>
		</div>
		<img
			src="/female_doctor_2.png"
			alt=""
			class="absolute bottom-0 right-0 lg:w-1/2 z-10 mt-12 doc hidden lg:block"
		/>
		<img
			src="/ellipse1.png"
			alt="ellipse"
			class="absolute bottom-0 right-0 lg:w-1/2 ellilpse hidden lg:block"
		/>
	</div>
	<Services />
	<div
		id="team"
		class="h-screen flex items-center text-center lg:text-left third-screen lg:pt-0 mb-0 md:mb-16 lg:mb-0"
	>
		<div class="lg:flex flex-row rounded items-center justify-between lg:content-center">
			<div class="lg:w-1/2 flex justify-center order-last lg:order-first">
				<img
					src="https://online.norwich.edu/sites/default/files/content/resources/header/157.jpg"
					alt="team"
					class="rounded-3xl w-2/3 team-picture hidden lg:block"
				/>
			</div>
			<div class="lg:w-1/2 lg:p-5 p-2 team-container">
				<h3 class=" bold text-lime-600">Tot uw dienst</h3>
				<h2 class=" text-2xl my-4">Maak kennis met ons zorgzame team</h2>
				<!-- <p class="text-md lg:w-1/2 my-3 mx-2 lg:mx-0"></p> -->
				<p class="text-md">
					Ons toegewijde team staat volledig tot uw dienst om hoogwaardige zorg te bieden. We
					begrijpen dat uw welzijn van het grootste belang is en streven ernaar om u de beste
					zorgervaring te bieden. Met een team van ervaren professionals zijn we uitgerust om aan al
					uw zorgbehoeften te voldoen.
				</p>
				<div class="mt-5 flex flew-row justify-center lg:justify-start">
					<img src="/check-icon.png" alt="" />
					<p class="bold text-md font-medium px-3">Experten</p>
				</div>
				<div class="mt-3 flex flew-row justify-center lg:justify-start">
					<img src="/check-icon.png" alt="" />
					<p class="bold text-md font-medium px-3">+20 jaar ervaring</p>
				</div>
			</div>

			<div class="w-5/6 flex justify-center order-last lg:hidden mx-auto mt-4">
				<img
					src="https://online.norwich.edu/sites/default/files/content/resources/header/157.jpg"
					alt="team"
					class="rounded-3xl p-3 team-picture md:w-3/5 lg:hidden block"
				/>
			</div>
		</div>
	</div>
	<div
		id="review"
		class=" mb-0 md:mb-32 sm fourth-screen lg:mb-0 h-screen mt-0 lg:flex lg:flex-col lg:content-center lg:justify-center"
	>
		<h3 class="text-center bold text-lime-600 mt-16 lg:mt-0 title-review">Onze Beoordeling</h3>
		<!-- <h2 class="text-center text-2xl my-4 px-2">
			Nova heeft een ruim zorgaanbod voor elke persoon die aangesloten is bij een Belgische
			mutualiteit.
		</h2> -->
		<div
			class="lg:flex lg:flex-row justify-center lg:gap-8 lg:max-w-6xl lg:my-24 diensten mx-auto lg:justify-between container-review"
		>
			<div
				class="border-t-4 border-lime-600 rounded-md mx-auto shadow-lg w-80 lg:w-80 md:w-64 h-56 lg:h-64 py-5 lg:py-10 lg:my-0 my-8 text-center lg:text-left md:text-left flex flex-col gap-4 justify-center"
			>
				<h3 class="py-2 text-4xl lg:text-5xl text-center">6</h3>
				<h4 class="text-center">Geverifieerde specialisten</h4>
			</div>
			<div
				class="border-t-4 border-lime-600 rounded-md mx-auto shadow-lg w-80 lg:w-80 md:w-64 h-56 lg:h-64 py-5 lg:py-10 lg:my-0 my-8 text-center lg:text-left md:text-left flex flex-col gap-4 justify-center"
			>
				<!-- <h3 class="py-2 text-4xl lg:text-5xl text-center" this:value={count} /> -->
				<h3 class="py-2 text-4xl lg:text-5xl text-center">+50</h3>
				<h4 class="text-center">Tevreden klanten</h4>
			</div>
			<div
				class="border-t-4 border-lime-600 rounded-md mx-auto shadow-lg w-80 lg:w-80 h-56 md:w-64 lg:h-64 py-5 lg:py-10 lg:my-0 my-8 text-center lg:text-left md:text-left flex flex-col gap-4 justify-center"
			>
				<h3 class="py-2 text-4xl lg:text-5xl text-center">99,7%</h3>
				<h4 class="text-center">Positieve feedback</h4>
			</div>
		</div>
	</div>
	<div
		id="contact"
		class="mb-0 md:mb-32 lg:mb-0 h-screen last-screen lg:flex lg:flex-col justify-center"
	>
		<h3 class="text-center font-bold text-lime-600 mt-16 lg:mt-0 contact-title1">Contacteer ons</h3>
		<h2 class="text-center text-2xl my-4 mb-8 lg:mb-16 px-2 contact-title2">
			Wenst u thuisverpleging aan te vragen, gebruik te maken van onze ondersteunende diensten of
			heeft u een vraag? Aarzel dan niet om ons te contacteren!
		</h2>
		<div class="flex flex-col lg:flex-row lg:justify-between sm:justify-center">
			<div
				class="flex flex-col lg:items-start items-center mb-8 lg:mb-0 lg:justify-center lg:min-w-fit lg:px-4 lg:ml-8 contact-container"
			>
				<div class="flex flex-row items-center mb-4 justify-between">
					<img src="/phone-solid.svg" alt="" class="w-8 mx-2 lg:mx-0 lg:w-12 lg:mr-4" />
					<a href="tel:+31612345678">+0473 95 28 64</a>
				</div>

				<div class="flex flex-row items-center mb-4 justify-between">
					<img src="/envelope-solid.svg" alt="" class="w-8 mx-2 lg:mx-0 lg:w-12 lg:mr-4" />

					<a href="mailto:lyhxr@example.com">info@norwich.edu</a>
				</div>
			</div>
			<div class="mx-2 lg:w-full form-container">
				<form
					action="https://formspree.io/f/xgejwpke"
					method="POST"
					class="max-w-lg lg:max-w-4xl mx-auto"
				>
					<div class="mb-4">
						<label for="name" class="block text-gray-700 font-semibold">Naam</label>
						<input
							type="text"
							id="name"
							name="name"
							class="w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-lime-600"
							required
						/>
					</div>
					<div class="mb-4">
						<label for="email" class="block text-gray-700 font-semibold">E-mailadres</label>
						<input
							type="email"
							id="email"
							name="email"
							class="w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-lime-600"
							required
						/>
					</div>
					<div class="mb-4">
						<label for="message" class="block text-gray-700 font-semibold">Bericht</label>
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
						class="py-3 px-5 bg-lime-600 hover:bg-lime-500 text-white rounded-lg send-btn"
						>Verzenden</button
					>
				</form>
			</div>
		</div>
	</div>
</main>
<footer class="bg-gray-200 py-4 mt-8 lg:mt-8">
	<div class="lg:px-24">
		<div class="flex justify-center">
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
	.send-btn {
		transition: background-color 0.3s ease;
	}
</style>
