<script>
	import '@fontsource-variable/geist';
	let { children } = $props();
</script>

{@render children()}

<style>
	:global(*) {
		box-sizing: border-box;
		margin: 0;
		padding: 0;
	}
	:global(:root) {
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
		--gpnk: #ffd1ff;

		--radius-md: 0.375rem;
		--radius-xl: 0.75rem;
		--text-xs: 0.6rem;
		--text-sm: 0.75rem;
		--text-base: 1rem;
		--text-2xl: 1.5rem;

		background-color: var(--bg);
		color-scheme: light dark;
		font-family: 'Geist Varialbe', monospace;
	}
</style>
