<script>
	import { fly } from 'svelte/transition';
	import { fade } from 'svelte/transition';
	import { slide } from 'svelte/transition';
	let counter = 0;
	// let visible = true;
	function counterIncrease() {
		counter += 1;
		if (counter == 4) {
			counter = 0;
		}
	}
	function counterDecrease() {
		counter -= 1;
		if (counter < 0) {
			counter = 3;
		}
	}
</script>

<div
	id="diensten"
	class="mb-32 second-screen md:mb-56 lg:mb-0 h-full lg:h-screen lg:flex lg:flex-col lg:content-center lg:justify-center"
>
	<div>
		<h3 class="text-center bold text-lime-600 mt-16 lg:mt-0 title-diensten">Onze Diensten</h3>
		<h2 class="text-center text-2xl my-4 px-2 title-diensten-2">
			Nova heeft een ruim zorgaanbod voor elke persoon die aangesloten is bij een Belgische
			mutualiteit.
		</h2>

		{#if counter == 0}
			<div
				in:slide|local={{ duration: 500, axis: 'x' }}
				class="lg:flex lg:flex-row justify-center lg:max-w-6xl lg:my-24 diensten mx-auto lg:justify-between container-diensten p-2"
			>
				<div
					class="flex flex-col justify-center lg:block border-t-4 border-lime-600 rounded-md mx-auto shadow-lg w-80 h-56 lg:h-64 py-5 lg:py-10 px-8 lg:my-0 my-8 text-center lg:text-left md:text-left"
				>
					<img
						src="/soap-solid.svg"
						alt="support icon"
						class="lg:py-2 lg:w-12 md:w-10 w-8 lg:mx-0 mx-auto hidden lg:block md:block"
					/>
					<h3 class="py-2 text-lg lg:text-xl">Hygiënische zorgen</h3>
					<p class="text-sm lg:py-2">Zorg voor een goede persoonlijke hygiëne.</p>
				</div>
				<div
					class="flex flex-col justify-center lg:block border-t-4 border-lime-600 rounded-md mx-auto shadow-lg w-80 h-56 lg:h-64 py-5 lg:py-10 px-8 lg:my-0 my-8 text-center lg:text-left md:text-left"
				>
					<img
						src="/bandage-solid.svg"
						alt="bandage icon"
						class="lg:py-2 lg:mx-0 lg:w-12 md:w-10 w-8 mx-auto hidden lg:block md:block"
					/>
					<h3 class="py-2 text-lg lg:text-xl">Wondverzorging</h3>
					<p class="text-sm lg:py-2">Professionele zorg voor wonden.</p>
				</div>
				<div
					class="flex flex-col justify-center lg:block border-t-4 border-lime-600 rounded-md mx-auto shadow-lg w-80 h-56 lg:h-64 py-5 lg:py-10 px-8 lg:my-0 my-8 text-center lg:text-left md:text-left"
				>
					<img
						src="/sringe-solid.svg"
						alt="bandage icon"
						class="lg:py-2 lg:mx-0 lg:w-12 md:w-10 w-8 mx-auto hidden lg:block md:block"
					/>
					<h3 class="py-2 text-lg lg:text-xl">Inspuitingen</h3>
					<!-- injecties -->
					<p class="text-sm lg:py-2">Veilige toediening van injecties.</p>
				</div>
			</div>
			<div class="flex items-center gap-10 justify-center">
				<button
					type="submit"
					class="py-3 px-2 w-24 lg:px-3 lg:py-3 bg-lime-600 hover:bg-lime-500 text-white rounded-lg send-btn"
					on:click={counterDecrease}>Vorige</button
				>
				<div class="flex gap-3 justify-between">
					<div class="rounded-full w-3 h-3 bg-gray-400" />
					<div class="rounded-full w-3 h-3 bg-gray-300" />
					<div class="rounded-full w-3 h-3 bg-gray-300" />
					<div class="rounded-full w-3 h-3 bg-gray-300" />
				</div>
				<button
					type="submit"
					class="py-3 px-2 w-24 lg:px-3 lg:py-3 bg-lime-600 hover:bg-lime-500 text-white rounded-lg send-btn"
					on:click={counterIncrease}>Volgende</button
				>
			</div>
		{:else if counter == 1}
			<div
				in:slide|local={{ duration: 500, axis: 'x' }}
				class="lg:flex lg:flex-row justify-center lg:max-w-6xl lg:my-24 diensten mx-auto lg:justify-between container-diensten p-2"
			>
				<div
					class="flex flex-col justify-center lg:block border-t-4 border-lime-600 rounded-md mx-auto shadow-lg w-80 h-56 lg:h-64 py-5 lg:py-10 px-8 lg:my-0 my-8 text-center lg:text-left md:text-left"
				>
					<img
						src="/sock-solid.svg"
						alt="support icon"
						class="lg:py-2 lg:w-12 md:w-10 w-8 lg:mx-0 mx-auto"
					/>
					<h3 class="py-2 text-lg lg:text-xl">Compressiekousen</h3>
					<p class="text-sm lg:py-2">Professionele ondersteuning met compressiekousen.</p>
				</div>
				<div
					class="flex flex-col justify-center lg:block border-t-4 border-lime-600 rounded-md mx-auto shadow-lg w-80 h-56 lg:h-64 py-5 lg:py-10 px-8 lg:my-0 my-8 text-center lg:text-left md:text-left"
				>
					<img
						src="/sringe-solid.svg"
						alt="bandage icon"
						class="lg:py-2 lg:mx-0 lg:w-12 md:w-10 w-8 mx-auto hidden lg:block md:block"
					/>
					<h3 class="py-2 text-lg lg:text-xl">Insuline injecteren</h3>
					<p class="text-sm lg:py-2">Deskundige insuline-injecties verzorgen.</p>
				</div>
				<div
					class="flex flex-col justify-center lg:block border-t-4 border-lime-600 rounded-md mx-auto shadow-lg w-80 h-56 lg:h-64 py-5 lg:py-10 px-8 lg:my-0 my-8 text-center lg:text-left md:text-left"
				>
					<img
						src="/bandage-solid.svg"
						alt="bandage icon"
						class="lg:py-2 lg:mx-0 lg:w-12 md:w-10 w-8 mx-auto hidden lg:block md:block"
					/>
					<h3 class="py-2 text-lg lg:text-xl">Compressieverband</h3>
					<p class="text-sm lg:py-2">Effectieve behandeling met compressieverband.</p>
				</div>
			</div>
			<div class="flex items-center gap-10 justify-center">
				<button
					type="submit"
					class="py-3 px-3 w-24 bg-lime-600 hover:bg-lime-500 text-white rounded-lg send-btn"
					on:click={counterDecrease}>Vorige</button
				>
				<div class="flex gap-3 justify-between">
					<div class="rounded-full w-3 h-3 bg-gray-300" />
					<div class="rounded-full w-3 h-3 bg-gray-400" />
					<div class="rounded-full w-3 h-3 bg-gray-300" />
					<div class="rounded-full w-3 h-3 bg-gray-300" />
				</div>
				<button
					type="submit"
					class="py-3 px-2 w-24 lg:px-3 lg:py-3 bg-lime-600 hover:bg-lime-500 text-white rounded-lg send-btn"
					on:click={counterIncrease}>Volgende</button
				>
			</div>
		{:else if counter == 2}
			<div
				in:slide|local={{ duration: 500, axis: 'x' }}
				class="lg:flex lg:flex-row justify-center lg:max-w-6xl lg:my-24 diensten mx-auto lg:justify-between container-diensten p-2"
			>
				<div
					class="flex flex-col justify-center lg:block border-t-4 border-lime-600 rounded-md mx-auto shadow-lg w-80 h-56 lg:h-64 py-5 lg:py-10 px-8 lg:my-0 my-8 text-center lg:text-left md:text-left"
				>
					<img
						src="/care-solid.svg"
						alt="support icon"
						class="lg:py-2 lg:w-12 md:w-10 w-8 lg:mx-0 mx-auto lg:block md:block"
					/>
					<h3 class="py-2 text-lg lg:text-xl">Stomazorg</h3>
					<p class="text-sm lg:py-2">Betrouwbare zorg voor stoma-patiënten.</p>
				</div>
				<div
					class="flex flex-col justify-center lg:block border-t-4 border-lime-600 rounded-md mx-auto shadow-lg w-80 h-56 lg:h-64 py-5 lg:py-10 px-8 lg:my-0 my-8 text-center lg:text-left md:text-left"
				>
					<img
						src="/eye-drop.svg"
						alt="bandage icon"
						class="lg:py-2 lg:mx-0 lg:w-12 md:w-10 w-8 mx-auto hidden lg:block md:block"
					/>
					<h3 class="py-2 text-lg lg:text-xl">Oogdruppels</h3>
					<p class="text-sm lg:py-2">Zorgvuldige toediening van oogdruppels.</p>
				</div>
				<div
					class="flex flex-col justify-center lg:block border-t-4 border-lime-600 rounded-md mx-auto shadow-lg w-80 h-56 lg:h-64 py-5 lg:py-10 px-8 lg:my-0 my-8 text-center lg:text-left md:text-left"
				>
					<img
						src="/zalf.svg"
						alt="bandage icon"
						class="lg:py-2 lg:mx-0 lg:w-12 md:w-10 w-8 mx-auto hidden lg:block md:block"
					/>
					<h3 class="py-2 text-lg lg:text-xl">Zalven</h3>
					<p class="text-sm lg:py-2">Deskundig aanbrengen van zalf.</p>
				</div>
			</div>
			<div class="flex items-center gap-10 justify-center">
				<button
					type="submit"
					class="py-3 px-3 w-24 bg-lime-600 hover:bg-lime-500 text-white rounded-lg send-btn"
					on:click={counterDecrease}>Vorige</button
				>
				<div class="flex gap-3 justify-between">
					<div class="rounded-full w-3 h-3 bg-gray-300" />
					<div class="rounded-full w-3 h-3 bg-gray-300" />
					<div class="rounded-full w-3 h-3 bg-gray-400" />
					<div class="rounded-full w-3 h-3 bg-gray-300" />
				</div>
				<button
					type="submit"
					class="py-3 px-2 w-24 lg:px-3 lg:py-3 bg-lime-600 hover:bg-lime-500 text-white rounded-lg send-btn"
					on:click={counterIncrease}>Volgende</button
				>
			</div>
		{:else if counter == 3}
			<div
				in:slide|local={{ duration: 500, axis: 'x' }}
				class="lg:flex lg:flex-row justify-center lg:max-w-6xl lg:my-24 diensten mx-auto container-diensten p-2"
			>
				<div
					class="flex flex-col justify-center lg:block border-t-4 border-lime-600 rounded-md mx-auto shadow-lg w-80 h-56 lg:h-64 py-5 lg:py-10 px-8 lg:my-0 my-8 text-center lg:text-left md:text-left"
				>
					<img
						src="/medication.svg"
						alt="support icon"
						class="lg:py-2 lg:w-12 md:w-10 w-8 lg:mx-0 mx-auto hidden lg:block md:block"
					/>
					<h3 class="py-2 text-lg lg:text-xl">Voorbereiden van weekmedicatie</h3>
					<p class="text-sm lg:py-2">Nauwkeurige voorbereiding van wekelijkse medicatie.</p>
				</div>
				<div
					class="flex flex-col justify-center lg:block border-t-4 border-lime-600 rounded-md mx-auto shadow-lg w-80 h-56 lg:h-64 py-5 lg:py-10 px-8 lg:my-0 my-8 text-center lg:text-left md:text-left"
				>
					<img
						src="/support-solid.svg"
						alt="bandage icon"
						class="lg:py-2 lg:mx-0 lg:w-12 md:w-10 w-8 mx-auto hidden lg:block md:block"
					/>
					<h3 class="py-2 text-lg lg:text-xl">Palliatieve verzorging</h3>
					<p class="text-sm lg:py-2">Empathische zorg voor palliatieve patiënten.</p>
				</div>
			</div>
			<div class="flex items-center gap-10 justify-center">
				<button
					type="submit"
					class="py-3 w-24 px-3 bg-lime-600 hover:bg-lime-500 text-white rounded-lg send-btn"
					on:click={counterDecrease}>Vorige</button
				>
				<div class="flex gap-3 justify-between">
					<div class="rounded-full w-3 h-3 bg-gray-300" />
					<div class="rounded-full w-3 h-3 bg-gray-300" />
					<div class="rounded-full w-3 h-3 bg-gray-300" />
					<div class="rounded-full w-3 h-3 bg-gray-400" />
				</div>
				<button
					type="submit"
					class="py-3 w-24 px-2 lg:px-3 lg:py-3 bg-lime-600 hover:bg-lime-500 text-white rounded-lg send-btn"
					on:click={counterIncrease}>Volgende</button
				>
			</div>
		{/if}
	</div>
</div>
