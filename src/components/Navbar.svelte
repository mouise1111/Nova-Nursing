<script>
	function scrollIntoView({ target }) {
		const el = document.querySelector(target.getAttribute('href'));
		if (!el) return;
		el.scrollIntoView({
			behavior: 'smooth'
		});
	}
</script>

<a
	href="#home"
	on:click|preventDefault={scrollIntoView}
	class="px-2 text-lg font-semibold lg:hidden md:hidden text-lime-600 hover:text-lime-700">Nova</a
>
<nav class="fixed z-50 hidden w-full lg:flex md:flex backdrop-blur-sm">
	<div class="w-full lg:px-24 md:px-4">
		<div class="flex items-center justify-between w-full h-16">
			<div class="flex-shrink-0">
				<a
					href="#home"
					on:click|preventDefault={scrollIntoView}
					class="text-lg font-semibold text-lime-600 hover:text-lime-700">Nova</a
				>
			</div>
			<div class="items-baseline hidden ml-10 space-x-4 md:flex lg:flex">
				<a
					href="#diensten"
					on:click|preventDefault={scrollIntoView}
					class="px-3 py-2 text-sm rounded-md hover:text-lime-950">Diensten</a
				>
				<a
					href="#team"
					on:click|preventDefault={scrollIntoView}
					class="px-3 py-2 text-sm rounded-md hover:text-lime-950">Over ons</a
				>
				<a
					href="#review"
					on:click|preventDefault={scrollIntoView}
					class="px-3 py-2 text-sm rounded-md hover:text-lime-950">Beoordelingen</a
				>
				<a
					href="#contact"
					on:click|preventDefault={scrollIntoView}
					class="px-3 py-2 text-sm rounded-md hover:text-lime-950">Contact</a
				>
			</div>
		</div>
	</div>
</nav>

<style>
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
