<script>
	function scrollIntoView({ target }) {
		const el = document.querySelector(target.getAttribute('href'));
		if (!el) return;
		el.scrollIntoView({
			behavior: 'smooth'
		});
	}
</script>

<nav class="">
	<div class="px-2 lg:px-0 md:px-4">
		<div class="flex items-center justify-between h-16">
			<div class="flex-shrink-0">
				<a href="#" class="text-lg font-semibold text-lime-600 hover:text-lime-700">Nova</a>
			</div>
			<div class="hidden md:block lg:block">
				<div class="ml-10 flex items-baseline space-x-4">
					<!-- <a href="#" class="px-3 py-2 rounded-md text-sm">Home</a> -->
					<a
						href="#diensten"
						on:click|preventDefault={scrollIntoView}
						class="px-3 py-2 rounded-md text-sm hover:text-lime-950">Diensten</a
					>
					<a
						href="#team"
						on:click|preventDefault={scrollIntoView}
						class="px-3 py-2 rounded-md text-sm hover:text-lime-950">Over ons</a
					>
					<a
						href="#review"
						on:click|preventDefault={scrollIntoView}
						class="px-3 py-2 rounded-md text-sm hover:text-lime-950">Beoordelingen</a
					>
					<a
						href="#contact"
						on:click|preventDefault={scrollIntoView}
						class="px-3 py-2 rounded-md text-sm hover:text-lime-950">Contact</a
					>
				</div>
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
