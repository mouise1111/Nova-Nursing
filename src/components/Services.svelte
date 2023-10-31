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
	class="h-full mb-32 second-screen md:mb-56 lg:mb-0 lg:h-screen lg:flex lg:flex-col lg:content-center lg:justify-center"
>
	<div>
		<h3 class="mt-16 text-center bold text-lime-600 lg:mt-0 title-diensten">Onze Diensten</h3>
		<h2 class="px-2 my-4 text-2xl text-center title-diensten-2">
			Nova heeft een ruim zorgaanbod voor elke persoon die aangesloten is bij een Belgische
			mutualiteit.
		</h2>

		{#if counter == 0}
			<div
				in:slide|local={{ duration: 500, axis: 'x' }}
				class="justify-center p-2 mx-auto lg:flex lg:flex-row lg:max-w-6xl lg:my-24 diensten lg:justify-between container-diensten"
			>
				<div
					class="flex flex-col justify-center h-56 px-8 py-5 mx-auto my-8 text-center border-t-4 rounded-md shadow-lg lg:block border-lime-600 w-80 lg:h-64 lg:py-10 lg:my-0 lg:text-left md:text-left"
				>
					<img
						src="/soap-solid.svg"
						alt="support icon"
						class="hidden w-8 mx-auto lg:py-2 lg:w-12 md:w-10 lg:mx-0 lg:block md:block"
					/>
					<h3 class="py-2 text-lg lg:text-xl">Hygiënische zorgen</h3>
					<p class="text-sm lg:py-2">Zorg voor een goede persoonlijke hygiëne.</p>
				</div>
				<div
					class="flex flex-col justify-center h-56 px-8 py-5 mx-auto my-8 text-center border-t-4 rounded-md shadow-lg lg:block border-lime-600 w-80 lg:h-64 lg:py-10 lg:my-0 lg:text-left md:text-left"
				>
					<img
						src="/bandage-solid.svg"
						alt="bandage icon"
						class="hidden w-8 mx-auto lg:py-2 lg:mx-0 lg:w-12 md:w-10 lg:block md:block"
					/>
					<h3 class="py-2 text-lg lg:text-xl">Wondverzorging</h3>
					<p class="text-sm lg:py-2">Professionele zorg voor wonden.</p>
				</div>
				<div
					class="flex flex-col justify-center h-56 px-8 py-5 mx-auto my-8 text-center border-t-4 rounded-md shadow-lg lg:block border-lime-600 w-80 lg:h-64 lg:py-10 lg:my-0 lg:text-left md:text-left"
				>
					<img
						src="/sringe-solid.svg"
						alt="bandage icon"
						class="hidden w-8 mx-auto lg:py-2 lg:mx-0 lg:w-12 md:w-10 lg:block md:block"
					/>
					<h3 class="py-2 text-lg lg:text-xl">Inspuitingen</h3>
					<!-- injecties -->
					<p class="text-sm lg:py-2">Veilige toediening van injecties.</p>
				</div>
			</div>
			<div class="flex items-center justify-center gap-5 lg:gap-10">
				<button
					type="submit"
					class="w-24 px-2 py-3 text-white rounded-lg lg:px-3 lg:py-3 bg-lime-600 hover:bg-lime-500 send-btn"
					on:click={counterDecrease}>Vorige</button
				>
				<div class="flex justify-between gap-3">
					<div class="w-3 h-3 bg-gray-400 rounded-full" />
					<div class="w-3 h-3 bg-gray-300 rounded-full" />
					<div class="w-3 h-3 bg-gray-300 rounded-full" />
					<div class="w-3 h-3 bg-gray-300 rounded-full" />
				</div>
				<button
					type="submit"
					class="w-24 px-2 py-3 text-white rounded-lg lg:px-3 lg:py-3 bg-lime-600 hover:bg-lime-500 send-btn"
					on:click={counterIncrease}>Volgende</button
				>
			</div>
		{:else if counter == 1}
			<div
				in:slide|local={{ duration: 500, axis: 'x' }}
				class="justify-center p-2 mx-auto lg:flex lg:flex-row lg:max-w-6xl lg:my-24 diensten lg:justify-between container-diensten"
			>
				<div
					class="flex flex-col justify-center h-56 px-8 py-5 mx-auto my-8 text-center border-t-4 rounded-md shadow-lg lg:block border-lime-600 w-80 lg:h-64 lg:py-10 lg:my-0 lg:text-left md:text-left"
				>
					<img
						src="/sock-solid.svg"
						alt="support icon"
						class="hidden w-8 mx-auto lg:py-2 lg:w-12 md:w-10 lg:mx-0 lg:block md:block"
					/>
					<h3 class="py-2 text-lg lg:text-xl">Compressiekousen</h3>
					<p class="text-sm lg:py-2">Professionele ondersteuning met compressiekousen.</p>
				</div>
				<div
					class="flex flex-col justify-center h-56 px-8 py-5 mx-auto my-8 text-center border-t-4 rounded-md shadow-lg lg:block border-lime-600 w-80 lg:h-64 lg:py-10 lg:my-0 lg:text-left md:text-left"
				>
					<img
						src="/sringe-solid.svg"
						alt="bandage icon"
						class="hidden w-8 mx-auto lg:py-2 lg:mx-0 lg:w-12 md:w-10 lg:block md:block"
					/>
					<h3 class="py-2 text-lg lg:text-xl">Insuline injecteren</h3>
					<p class="text-sm lg:py-2">Deskundige insuline-injecties verzorgen.</p>
				</div>
				<div
					class="flex flex-col justify-center h-56 px-8 py-5 mx-auto my-8 text-center border-t-4 rounded-md shadow-lg lg:block border-lime-600 w-80 lg:h-64 lg:py-10 lg:my-0 lg:text-left md:text-left"
				>
					<img
						src="/bandage-solid.svg"
						alt="bandage icon"
						class="hidden w-8 mx-auto lg:py-2 lg:mx-0 lg:w-12 md:w-10 lg:block md:block"
					/>
					<h3 class="py-2 text-lg lg:text-xl">Compressieverband</h3>
					<p class="text-sm lg:py-2">Effectieve behandeling met compressieverband.</p>
				</div>
			</div>
			<div class="flex items-center justify-center gap-5 lg:gap-10">
				<button
					type="submit"
					class="w-24 px-3 py-3 text-white rounded-lg bg-lime-600 hover:bg-lime-500 send-btn"
					on:click={counterDecrease}>Vorige</button
				>
				<div class="flex justify-between gap-3">
					<div class="w-3 h-3 bg-gray-300 rounded-full" />
					<div class="w-3 h-3 bg-gray-400 rounded-full" />
					<div class="w-3 h-3 bg-gray-300 rounded-full" />
					<div class="w-3 h-3 bg-gray-300 rounded-full" />
				</div>
				<button
					type="submit"
					class="w-24 px-2 py-3 text-white rounded-lg lg:px-3 lg:py-3 bg-lime-600 hover:bg-lime-500 send-btn"
					on:click={counterIncrease}>Volgende</button
				>
			</div>
		{:else if counter == 2}
			<div
				in:slide|local={{ duration: 500, axis: 'x' }}
				class="justify-center p-2 mx-auto lg:flex lg:flex-row lg:max-w-6xl lg:my-24 diensten lg:justify-between container-diensten"
			>
				<div
					class="flex flex-col justify-center h-56 px-8 py-5 mx-auto my-8 text-center border-t-4 rounded-md shadow-lg lg:block border-lime-600 w-80 lg:h-64 lg:py-10 lg:my-0 lg:text-left md:text-left"
				>
					<img
						src="/care-solid.svg"
						alt="support icon"
						class="hidden w-8 mx-auto lg:py-2 lg:w-12 md:w-10 lg:mx-0 lg:block md:block"
					/>
					<h3 class="py-2 text-lg lg:text-xl">Stomazorg</h3>
					<p class="text-sm lg:py-2">Betrouwbare zorg voor stoma-patiënten.</p>
				</div>
				<div
					class="flex flex-col justify-center h-56 px-8 py-5 mx-auto my-8 text-center border-t-4 rounded-md shadow-lg lg:block border-lime-600 w-80 lg:h-64 lg:py-10 lg:my-0 lg:text-left md:text-left"
				>
					<img
						src="/eye-drop.svg"
						alt="bandage icon"
						class="hidden w-8 mx-auto lg:py-2 lg:mx-0 lg:w-12 md:w-10 lg:block md:block"
					/>
					<h3 class="py-2 text-lg lg:text-xl">Oogdruppels</h3>
					<p class="text-sm lg:py-2">Zorgvuldige toediening van oogdruppels.</p>
				</div>
				<div
					class="flex flex-col justify-center h-56 px-8 py-5 mx-auto my-8 text-center border-t-4 rounded-md shadow-lg lg:block border-lime-600 w-80 lg:h-64 lg:py-10 lg:my-0 lg:text-left md:text-left"
				>
					<img
						src="/zalf.svg"
						alt="bandage icon"
						class="hidden w-8 mx-auto lg:py-2 lg:mx-0 lg:w-12 md:w-10 lg:block md:block"
					/>
					<h3 class="py-2 text-lg lg:text-xl">Zalven</h3>
					<p class="text-sm lg:py-2">Deskundig aanbrengen van zalf.</p>
				</div>
			</div>
			<div class="flex items-center justify-center gap-5 lg:gap-10">
				<button
					type="submit"
					class="w-24 px-3 py-3 text-white rounded-lg bg-lime-600 hover:bg-lime-500 send-btn"
					on:click={counterDecrease}>Vorige</button
				>
				<div class="flex justify-between gap-3">
					<div class="w-3 h-3 bg-gray-300 rounded-full" />
					<div class="w-3 h-3 bg-gray-300 rounded-full" />
					<div class="w-3 h-3 bg-gray-400 rounded-full" />
					<div class="w-3 h-3 bg-gray-300 rounded-full" />
				</div>
				<button
					type="submit"
					class="w-24 px-2 py-3 text-white rounded-lg lg:px-3 lg:py-3 bg-lime-600 hover:bg-lime-500 send-btn"
					on:click={counterIncrease}>Volgende</button
				>
			</div>
		{:else if counter == 3}
			<div
				in:slide|local={{ duration: 500, axis: 'x' }}
				class="justify-center p-2 mx-auto lg:flex lg:flex-row lg:max-w-6xl lg:my-24 diensten container-diensten"
			>
				<div
					class="flex flex-col justify-center h-56 px-8 py-5 mx-auto my-8 text-center border-t-4 rounded-md shadow-lg lg:block border-lime-600 w-80 lg:h-64 lg:py-10 lg:my-0 lg:text-left md:text-left"
				>
					<img
						src="/medication.svg"
						alt="support icon"
						class="hidden w-8 mx-auto lg:py-2 lg:w-12 md:w-10 lg:mx-0 lg:block md:block"
					/>
					<h3 class="py-2 text-lg lg:text-xl">Voorbereiden van weekmedicatie</h3>
					<p class="text-sm lg:py-2">Nauwkeurige voorbereiding van wekelijkse medicatie.</p>
				</div>
				<div
					class="flex flex-col justify-center h-56 px-8 py-5 mx-auto my-8 text-center border-t-4 rounded-md shadow-lg lg:block border-lime-600 w-80 lg:h-64 lg:py-10 lg:my-0 lg:text-left md:text-left"
				>
					<img
						src="/support-solid.svg"
						alt="bandage icon"
						class="hidden w-8 mx-auto lg:py-2 lg:mx-0 lg:w-12 md:w-10 lg:block md:block"
					/>
					<h3 class="py-2 text-lg lg:text-xl">Palliatieve verzorging</h3>
					<p class="text-sm lg:py-2">Empathische zorg voor palliatieve patiënten.</p>
				</div>
			</div>
			<div class="flex items-center justify-center gap-5 lg:gap-10">
				<button
					type="submit"
					class="w-24 px-3 py-3 text-white rounded-lg bg-lime-600 hover:bg-lime-500 send-btn"
					on:click={counterDecrease}>Vorige</button
				>
				<div class="flex justify-between gap-3">
					<div class="w-3 h-3 bg-gray-300 rounded-full" />
					<div class="w-3 h-3 bg-gray-300 rounded-full" />
					<div class="w-3 h-3 bg-gray-300 rounded-full" />
					<div class="w-3 h-3 bg-gray-400 rounded-full" />
				</div>
				<button
					type="submit"
					class="w-24 px-2 py-3 text-white rounded-lg lg:px-3 lg:py-3 bg-lime-600 hover:bg-lime-500 send-btn"
					on:click={counterIncrease}>Volgende</button
				>
			</div>
		{/if}
	</div>
</div>
