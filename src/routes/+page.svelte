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
	:global(*) {
		box-sizing: border-box;
		margin: 0;
		padding: 0;
	}
	:root {
		--bg-dark: #0a0a0a;
		--bg-darker: #0d0d0d;
		--bg: #111111;
		--surface: #181818;
		--border: #404040;
		--fg: #e9e4e4;
		--red: #b76467;
		--green: #8d987e;
		--yellow: #dabd8d;
		--blue: #8ea4ba;
		--magenta: #aa89b1;
		--cyan: #8ba7a3;

		--gred: #fc466b;
		--gblu: #3f5efb;
		--gpnk: #efd5ff;

		background-color: var(--bg);
		color-scheme: light dark;
	}
	main {
		height: 100dvh;
		font-family: 'Geist Mono', Inter, system-ui, Avenir, Helvetica, Arial, sans-serif;
		font-weight: 400;
		line-height: 1.5;
		color: var(--fg);

		display: grid;
		place-items: center;
		grid-template-rows: 1fr auto;
	}
</style>
