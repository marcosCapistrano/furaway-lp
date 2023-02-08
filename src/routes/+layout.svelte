<script>
// @ts-nocheck

	import '../scss/styles.scss';
	import Header from './Header.svelte';
	import Footer from './Footer.svelte';
</script>

<Header />

<main>
	<slot />
</main>

<Footer />

<style>
</style>
