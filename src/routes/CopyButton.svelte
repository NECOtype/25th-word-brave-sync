<script lang="ts">
	import { wordOfTheDay } from '$lib/stores';
	import { get } from 'svelte/store';

	let label = $state<'Copy' | 'Copied!'>('Copy');
	let word = $derived(wordOfTheDay);

	async function handleCopy() {
		try {
			await navigator.clipboard.writeText(get(word));
			label = 'Copied!';
			setTimeout(() => (label = 'Copy'), 1000);
		} catch {
			alert('Failed to copy!');
		}
	}
</script>

<button onclick={handleCopy}>
	{label}
</button>

<style>
	button {
		color: var(--fg);
		font-family: inherit;
		background-color: var(--border);
		width: 6rem;
		padding: 0.5rem 1rem;
		font-weight: bold;
		text-align: center;
		border: 1px solid var(--border);
		border-radius: 0.5rem;

		&:hover {
			filter: brightness(85%);
			cursor: pointer;
		}
	}
</style>
