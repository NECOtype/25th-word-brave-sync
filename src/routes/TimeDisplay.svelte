<script lang="ts">
	import { onMount } from 'svelte';

	let currentTime: string;

	onMount(() => {
		const updateTime = () => {
			const date = new Date();

			const options: Intl.DateTimeFormatOptions = {
				weekday: 'short',
				year: 'numeric',
				month: 'long',
				day: '2-digit',
				hour: '2-digit',
				minute: '2-digit',
				second: '2-digit',
				timeZoneName: 'short',
				timeZone: 'Etc/GMT'
			};
			const formattedTime = new Intl.DateTimeFormat('en-GB', options).format(date);

			currentTime = formattedTime;
		};

		updateTime();
		setInterval(updateTime, 1000);
	});
</script>

<p>{currentTime}</p>

<style>
	p {
		font-size: var(--text-xs);
		filter: brightness(90%);
		grid-column-start: 1;
		grid-column-end: 3;
		padding-bottom: 0.5rem;
	}
</style>
