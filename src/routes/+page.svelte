<script>
	import gsap from 'gsap';
	import { ScrollTrigger } from 'gsap/dist/ScrollTrigger';
	import Scrollbar from 'smooth-scrollbar';
	import { onMount, setContext } from 'svelte';
	import Navbar from '../components/Navbar.svelte';
	onMount(() => {
		let tl = gsap.timeline({
			scrollTrigger: {
				trigger: 'team-picture'
			}
		});

		// tl.addLabel('start')
		// 	.from('.text-6xl', { x: 100, opacity: 0, ease: 'power' })
		// 	.from('.doc ', { scale: 0.3, rotation: 45, autoAlpha: 0 })
		// 	.from('.contact-btn', { x: -100, opacity: 0, ease: 'power' });
		// tl.fromTo(
		// 	'.diensten',
		// 	{ x: 100, opacity: 0, scrollTrigger: { start: '50%', end: '100%' } },
		// 	{ x: 0, opacity: 1 }
		// );

		tl.from('.team-picture', { y: 100, opacity: 0, ease: 'power' });
	});
</script>

<main class="lg:px-24 sm:w-full">
	<div class="h-3/4 lg:h-screen first-screen">
		<Navbar />
		<div class="lg:pt-16 pt-5">
			<!-- <h1 class="text-6xl tracking-wider font-extrabold my-3 sm:text-sm">
				Met een hart voor <span class="text-lime-600">Zorg</span>
			</h1> -->
			<h1 class="text-5xl md:text-5xl lg:text-6xl tracking-wider font-extrabold my-3 mx-2 lg:mx-0">
				Met een hart voor <span class="text-lime-600">Zorg</span>
			</h1>

			<h2 class="text-4xl font-bold tracking-wider my-5 mx-2 lg:mx-0 lg:text-left text-right">
				Thuisverpleging
			</h2>
			<p class="text-md lg:w-1/2 my-3 mx-2 lg:mx-0">
				Welkom bij Nova - Uw vertrouwde partner voor thuisverpleging. Onze toegewijde en ervaren
				verpleegkundigen bieden gepersonaliseerde zorg en ondersteuning in de comfortabele omgeving
				van uw eigen huis. Ontdek de Nova-difference en ervaar hoogwaardige thuisverpleging op maat.
			</p>
			<button class="py-3 px-5 bg-lime-600 text-white rounded-lg my-3 contact-btn mx-2 lg:mx-0">
				Contacteer ons
			</button>
		</div>
		<img
			src="/female_doctor_1.png"
			alt=""
			class="absolute bottom-0 right-0 lg:w-1/2 z-10 mt-12 doc hidden lg:block"
		/>
		<img
			src="/ellipse1.png"
			alt="ellipse"
			class="absolute bottom-0 right-0 lg:w-1/2 ellilpse hidden lg:block"
		/>
	</div>
	<div class="h-3/4 second-screen">
		<h3 class="text-center bold text-lime-600 mt-16 lg:mt-32">Onze Diensten</h3>
		<h2 class="text-center text-2xl my-4 px-2">
			Nova heeft een ruim zorgaanbod voor elke persoon die aangesloten is bij een Belgische
			mutualiteit.
		</h2>
		<div
			class="lg:flex lg:flex-row justify-center lg:max-w-6xl lg:my-24 diensten mx-auto lg:justify-between"
		>
			<div
				class="border-t-4 border-lime-600 rounded-md mx-auto shadow-lg w-80 h-56 lg:h-64 py-5 lg:py-10 px-8 lg:my-0 my-8 text-center lg:text-left md:text-left"
			>
				<img src="/Bandage.png" alt="bandage icon" class="lg:py-2 lg:mx-0 mx-auto" />
				<h3 class="py-2 text-lg lg:text-xl">Wondverzorging</h3>
				<p class="text-sm lg:py-2">
					Onze deskundige verpleegkundigen bieden professionele wondverzorging op maat. Vertrouw op
					onze zorg en expertise voor uw wondgenezing.
				</p>
			</div>
			<div
				class="border-t-4 border-lime-600 rounded-md mx-auto shadow-lg w-80 h-56 lg:h-64 py-5 lg:py-10 px-8 lg:my-0 my-8 text-center lg:text-left md:text-left"
			>
				<img src="/Bandage.png" alt="bandage icon" class="lg:py-2 lg:mx-0 mx-auto" />
				<h3 class="py-2 text-lg lg:text-xl">Wondverzorging</h3>
				<p class="text-sm lg:py-2">
					Onze deskundige verpleegkundigen bieden professionele wondverzorging op maat. Vertrouw op
					onze zorg en expertise voor uw wondgenezing.
				</p>
			</div>
			<div
				class="border-t-4 border-lime-600 rounded-md mx-auto shadow-lg w-80 h-56 lg:h-64 py-5 lg:py-10 px-8 lg:my-0 my-8 text-center lg:text-left md:text-left"
			>
				<img src="/Bandage.png" alt="bandage icon" class="lg:py-2 lg:mx-0 mx-auto" />
				<h3 class="py-2 text-lg lg:text-xl">Wondverzorging</h3>
				<p class="text-sm lg:py-2">
					Onze deskundige verpleegkundigen bieden professionele wondverzorging op maat. Vertrouw op
					onze zorg en expertise voor uw wondgenezing.
				</p>
			</div>
		</div>
	</div>
	<div class="h-screen flex items-center text-center lg:text-left third-screen">
		<div class="lg:flex flex-row rounded items-center justify-between lg:content-center">
			<div class="lg:w-1/2 flex justify-center order-last lg:order-first">
				<img
					src="https://online.norwich.edu/sites/default/files/content/resources/header/157.jpg"
					alt="picture of the team"
					class="rounded-3xl w-2/3 team-picture hidden lg:block"
				/>
			</div>
			<div class="lg:w-1/2 lg:p-5 p-2 tattie">
				<h3 class=" bold text-lime-600">Tot uw dienst</h3>
				<h2 class=" text-2xl my-4">Maak kennis met ons zorgzame team</h2>
				<!-- <p class="text-md lg:w-1/2 my-3 mx-2 lg:mx-0"></p> -->
				<p class="text-sm">
					Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quo adipisci magnam, eos facilis
					earum quia. Numquam id deserunt illum totam aliquid atque corrupti nisi placeat temporibus
					maiores. Soluta, sit ?
				</p>
				<div class="mt-5 flex flew-row justify-center lg:justify-start">
					<img src="/check-icon.png" alt="" />
					<p class="bold text-md font-medium px-3">Experten</p>
				</div>
				<div class="mt-3 flex flew-row justify-center lg:justify-start">
					<img src="/check-icon.png" alt="" />
					<p class="bold text-md font-medium px-3">+5 jaar ervaring</p>
				</div>
			</div>

			<div class="lg:w-1/2 flex justify-center order-last lg:order-first lg:hidden">
				<img
					src="https://online.norwich.edu/sites/default/files/content/resources/header/157.jpg"
					alt="picture of the team"
					class="rounded-3xl p-3 team-picture"
				/>
			</div>
		</div>
	</div>
	<div class="h-3/4 second-screen mb-32 lg:mb-64">
		<h3 class="text-center bold text-lime-600 mt-16 lg:mt-16">Onze Beoordeling</h3>
		<!-- <h2 class="text-center text-2xl my-4 px-2">
			Nova heeft een ruim zorgaanbod voor elke persoon die aangesloten is bij een Belgische
			mutualiteit.
		</h2> -->
		<div
			class="lg:flex lg:flex-row justify-center lg:max-w-6xl lg:my-24 diensten mx-auto lg:justify-between"
		>
			<div
				class="border-t-4 border-lime-600 rounded-md mx-auto shadow-lg w-80 h-56 lg:h-64 py-5 lg:py-10 lg:my-0 my-8 text-center lg:text-left md:text-left flex flex-col gap-4 justify-center"
			>
				<h3 class="py-2 text-4xl lg:text-5xl text-center">6</h3>
				<h4 class="text-center">Geverifieerde specialisten</h4>
			</div>
			<div
				class="border-t-4 border-lime-600 rounded-md mx-auto shadow-lg w-80 h-56 lg:h-64 py-5 lg:py-10 lg:my-0 my-8 text-center lg:text-left md:text-left flex flex-col gap-4 justify-center"
			>
				<h3 class="py-2 text-4xl lg:text-5xl text-center">+50</h3>
				<h4 class="text-center">Tevreden klanten</h4>
			</div>
			<div
				class="border-t-4 border-lime-600 rounded-md mx-auto shadow-lg w-80 h-56 lg:h-64 py-5 lg:py-10 lg:my-0 my-8 text-center lg:text-left md:text-left flex flex-col gap-4 justify-center"
			>
				<h3 class="py-2 text-4xl lg:text-5xl text-center">99,7%</h3>
				<h4 class="text-center">Positieve feedback</h4>
			</div>
		</div>
	</div>
	<div class="mb-32 last-screen">
		<h3 class="text-center font-bold text-lime-600 mt-16">Contacteer ons</h3>
		<h2 class="text-center text-2xl my-4 mb-8 lg:mb-16 px-2">
			Wenst u thuisverpleging aan te vragen, gebruik te maken van onze ondersteunende diensten of
			heeft u een vraag? Aarzel dan niet om ons te contacteren!
		</h2>
		<div class="flex flex-col lg:flex-row lg:justify-between sm:justify-center">
			<div
				class="flex flex-col lg:items-start items-center mb-8 lg:mb-0 lg:justify-center lg:min-w-fit lg:px-4 lg:ml-8"
			>
				<div class="flex flex-row items-center mb-4 justify-between">
					<img src="/phone-solid.svg" alt="" class="w-8 mx-2 lg:mx-0 lg:w-12 lg:mr-4" />
					<a href="tel:+31612345678">+31 612 345 678</a>
				</div>

				<div class="flex flex-row items-center mb-4 justify-between">
					<img src="/envelope-solid.svg" alt="" class="w-8 mx-2 lg:mx-0 lg:w-12 lg:mr-4" />
					<a href="mailto:lyhxr@example.com">info@norwich.edu</a>
				</div>
			</div>
			<div class="mx-2 lg:w-full">
				<form action="#" method="POST" class="max-w-lg lg:max-w-4xl mx-auto">
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
					<button type="submit" class="py-3 px-5 bg-lime-600 text-white rounded-lg"
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
	}
	nav a {
		position: relative;
	}

	nav a::before {
		position: absolute;
		bottom: -4px;
		left: 0;
		content: '';
		width: 0;
		height: 2px;
		/* background: var(--cyan); */
		background: #96cf1d;
		transition: all 250ms ease;
	}
	nav a:hover::before {
		width: 100%;
	}
</style>
