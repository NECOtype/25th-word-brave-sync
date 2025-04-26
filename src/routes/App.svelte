<script lang="ts">
	import Title from './Title.svelte';
	import CopyButton from './CopyButton.svelte';
	import TimeDisplay from './TimeDisplay.svelte';
	import WordDisplay from './WordDisplay.svelte';
	import WarningMessage from './WarningMessage.svelte';
</script>

<container>
	<div>
		<Title />
		<main>
			<WordDisplay />
			<CopyButton />
			<TimeDisplay />
		</main>
		<WarningMessage />
	</div>
</container>

<style>
	container {
		width: 400px;
		border: 1px solid var(--border);
		margin: auto;
		border-radius: var(--radius-xl);
		padding: 1rem;
		display: grid;
		grid-template-rows: 1fr auto;

		main {
			display: grid;
			grid-template-columns: 1fr auto;
			gap: 0.5rem;
		}
	}
</style>
