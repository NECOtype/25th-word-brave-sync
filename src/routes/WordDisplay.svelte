<script lang="ts">
	import { onMount } from 'svelte';
	import { bip39words } from '$lib/wordlist';
	import { wordOfTheDay } from '$lib/stores';

	let theWord: string;

	onMount(() => {
		const epoch = new Date(Date.UTC(2022, 4, 10));
		const now = new Date();
		const delta = Math.round((+now - +epoch) / (24 * 60 * 60 * 1000));

		if (delta < 0) {
			theWord = 'Invalid date...';
			return;
		}

		const the25thWord = bip39words[delta];
		theWord = the25thWord;
		wordOfTheDay.set(theWord);
	});
</script>

<div><span>{theWord}</span></div>

<style>
	@keyframes magic {
		from {
			background-position: 0% center;
		}

		to {
			background-position: -200% center;
		}
	}
	div {
		border: 1px solid var(--border);
		padding: 0.5rem 1rem;
		font-weight: bold;
		text-align: center;
		border-radius: var(--radius-md);

		& span {
			font-size: var(--text-base);
			animation: magic 3s linear infinite;
			background: linear-gradient(to right, var(--gred), var(--gpnk), var(--gblu), var(--gred));
			background-clip: text;
			-webkit-background-clip: text;
			-webkit-text-fill-color: transparent;
			white-space: no-wrap;
			background-size: 200%;
		}
	}
</style>
