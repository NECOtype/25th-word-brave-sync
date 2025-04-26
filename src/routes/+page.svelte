<script lang="ts">
	import App from './App.svelte';
	import Footer from './Footer.svelte';
</script>

<svelte:head>
	<meta name="description" content="Get 25th Word for Brave Sync" />
	<title>25th word for Brave Sync time-limited words</title>
</svelte:head>

<main>
	<App />
	<Footer />
</main>

<style>
	main {
		height: 100dvh;
		font-weight: 400;
		line-height: 1.5;
		color: var(--fg);

		display: grid;
		place-items: center;
		grid-template-rows: 1fr auto;
	}
</style>
