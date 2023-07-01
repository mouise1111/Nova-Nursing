<script>
	import '../app.css';
	import '@fontsource/manrope';
</script>

<slot />

<style>
	:global(body) {
		font-family: 'manrope';
		font-display: swap;
	}

	:global(main) {
		box-sizing: 0;
	}
	:global(h3) {
		font-family: 'manrope';
		font: 400;
		font-weight: bold;
	}
</style>
