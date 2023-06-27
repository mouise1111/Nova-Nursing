<script>
	import gsap from 'gsap';
	import { ScrollTrigger } from 'gsap/dist/ScrollTrigger';
	import Scrollbar from 'smooth-scrollbar';
	import { onMount, setContext } from 'svelte';
	onMount(() => {
		let tl = gsap.timeline({
			scrollTrigger: {
				trigger: '.h-screen',
				pin: true,
				start: 'top top',
				end: '+=500',
				scrub: 1,
				snap: {
					snapTo: 'labels', // snap to the closest label in the timeline
					duration: { min: 0.2, max: 3 }, // the snap animation should be at least 0.2 seconds, but no more than 3 seconds (determined by velocity)
					delay: 0.2, // wait 0.2 seconds from the last scroll event before doing the snapping
					ease: 'power1.inOut' // the ease of the snap animation ("power3" by default)
				}
			}
		});

		tl.addLabel('start')
			.from('.text-6xl', { x: 100, opacity: 0, ease: 'power' })
			.from('.doc ', { scale: 0.3, rotation: 45, autoAlpha: 0 })
			.from('.contact-btn', { x: -100, opacity: 0, ease: 'power' });
		tl.addLabel('second').from('.diensten', { y: 100, opacity: 0, ease: 'power', delay: 0.5 });
		tl.addLabel('third').from('.team-picture', { y: 100, opacity: 0, ease: 'power', delay: 0.75 });
	});
</script>

<main class="lg:px-24 sm:w-full">
	<div class="h-screen first-screen">
		<nav class="">
			<div class="sm:px-4 lg:px-0 md:px-4">
				<div class="flex items-center justify-between h-16">
					<div class="flex-shrink-0">
						<a href="#" class="text-lg font-semibold text-lime-600 hover:text-lime-700">Nova</a>
					</div>
					<div class="hidden md:block">
						<div class="ml-10 flex items-baseline space-x-4">
							<a href="#" class="px-3 py-2 rounded-md text-sm">Home</a>
							<a href="#" class="px-3 py-2 rounded-md text-sm">Diensten</a>
							<a href="#" class="px-3 py-2 rounded-md text-sm">Over ons</a>
							<a href="#" class="px-3 py-2 rounded-md text-sm">Contact</a>
						</div>
					</div>
				</div>
			</div>
		</nav>
		<div class="pt-16 sm:p-0">
			<h1 class="text-6xl tracking-wider font-extrabold my-3">
				Met een hart voor <span class="text-lime-600">Zorg</span>
			</h1>
			<h2 class="text-4xl font-bold tracking-wider my-5">Thuisverpleging</h2>
			<p class="text-md w-1/2 my-3">
				Welkom bij Nova - Uw vertrouwde partner voor thuisverpleging. Onze toegewijde en ervaren
				verpleegkundigen bieden gepersonaliseerde zorg en ondersteuning in de comfortabele omgeving
				van uw eigen huis. Ontdek de Nova-difference en ervaar hoogwaardige thuisverpleging op maat.
			</p>
			<button class="py-3 px-5 bg-lime-600 text-white rounded-lg my-3 contact-btn"
				>Contacteer ons</button
			>
		</div>
		<img src="/female_doctor_1.png" alt="" class="absolute bottom-0 right-0 w-1/2 z-10 doc" />
		<img src="/ellipse1.png" alt="ellipse" class="absolute bottom-0 right-0 w-1/2 ellilpse" />
		<!-- <img
			src="/female_doctor_1.png"
			alt=""
			class="absolute bottom-0 right-0 w-full sm:w-1/2 z-10 doc mt-12 sm:mt-0"
		/>
		<img
			src="/ellipse1.png"
			alt="ellipse"
			class="absolute bottom-0 right-0 w-full sm:w-1/2 ellilpse mt-12 sm:mt-0"
		/> -->
	</div>
	<div class="h-3/4 second-screen">
		<h3 class="text-center bold text-lime-600 mt-32">Onze Diensten</h3>
		<h2 class="text-center text-2xl my-4">
			Nova heeft een ruim zorgaanbod voor elke persoon die aangesloten is bij een Belgische
			mutualiteit.
		</h2>
		<div class="flex flex-row justify-between max-w-6xl mx-auto my-24 diensten">
			<div class="border-t-4 border-lime-600 rounded-md shadow-lg w-80 h-64 py-10 px-8">
				<img src="/Bandage.png" alt="bandage icon" class="py-2" />
				<h3 class="py-2">Wondverzorging</h3>
				<p class="text-sm py-2">
					Onze deskundige verpleegkundigen bieden professionele wondverzorging op maat. Vertrouw op
					onze zorg en expertise voor uw wondgenezing.
				</p>
			</div>
			<div class="border-t-4 border-lime-600 rounded-md shadow-lg w-80 h-64 py-10 px-8">
				<img src="/Bandage.png" alt="bandage icon" class="py-2" />
				<h3 class="py-2">Wondverzorging</h3>
				<p class="text-sm py-2">
					Onze deskundige verpleegkundigen bieden professionele wondverzorging op maat. Vertrouw op
					onze zorg en expertise voor uw wondgenezing.
				</p>
			</div>
			<div class="border-t-4 border-lime-600 rounded-md shadow-lg w-80 h-64 py-10 px-8">
				<img src="/Bandage.png" alt="bandage icon" class="py-2" />
				<h3 class="py-2">Wondverzorging</h3>
				<p class="text-sm py-2">
					Onze deskundige verpleegkundigen bieden professionele wondverzorging op maat. Vertrouw op
					onze zorg en expertise voor uw wondgenezing.
				</p>
			</div>
		</div>
	</div>
	<div class="h-screen flex items-center third-screen justify-center">
		<div class="flex flex-row rounded items-center justify-between">
			<div class="w-1/2 flex justify-center">
				<img
					src="https://online.norwich.edu/sites/default/files/content/resources/header/157.jpg"
					alt="picture of the team"
					class="rounded-3xl w-2/3 team-picture"
				/>
			</div>
			<div class="w-1/2 p-5 tattie">
				<h3 class=" bold text-lime-600">Tot uw dienst</h3>
				<h2 class=" text-2xl my-4 font-semibold">Maak kennis met ons zorgzame team</h2>
				<p class="text-sm">
					Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quo adipisci magnam, eos facilis
					earum quia. Numquam id deserunt illum totam aliquid atque corrupti nisi placeat temporibus
					maiores. Soluta, sit ?
				</p>
				<div class="mt-5 flex flew-row">
					<img src="/check-icon.png" alt="" />
					<p class="bold text-md font-medium px-3">Experten</p>
				</div>
				<div class="mt-3 flex flew-row">
					<img src="/check-icon.png" alt="" />
					<p class="bold text-md font-medium px-3">Experten</p>
				</div>
			</div>
		</div>
	</div>
	<div class="h-screen last-screen">
		<h3 class="text-center bold text-lime-600">Contacteer ons</h3>
		<h2 class="text-center text-2xl my-4 mb-18">
			Wenst u thuisverpleging aan te vragen, gebruik te maken van onze ondersteunende diensten of
			heeft u een vraag? Aarzel dan niet om ons te contacteren!
		</h2>
		<div class="flex flex-wrap mt-24">
			<div class="flex-column justify-between w-1/3 mb-8">
				<div class="flex flex-row items-center">
					<img src="/Call.png" alt="" class="px-5" />
					<a href="tel:+31612345678">+31 612 345 678</a>
				</div>

				<div class="flex flex-row items-center">
					<img src="/Email.png" alt="" />
					<a href="mailto:lyhxr@example.com">info@norwich.edu</a>
				</div>
			</div>
			<div class="w-2/3">
				<form action="#" method="POST" class="max-w-lg mx-auto">
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
<footer class="bg-gray-200 py-4">
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
