<script>
	import { onDestroy, onMount } from 'svelte';

	// Props (actions)
	/** Provide the array of values to tick through. */
	export let values = [];
	/** Bind to the current value of the counter. */
	export let currentValue = '';

	/** Select items by index from the values array. */
	export let index = 0;

	let transitionInterval;

	$: currentValue = values[index];

	onMount(() => {
		transitionInterval = setInterval(() => {
			if (index === values.length - 1 || index > values.length - 1) {
				index = 0;
			} else {
				index = index + 1;
			}
		}, 1500);
	});

	onDestroy(() => {
		clearInterval(transitionInterval);
	});
</script>

{#key currentValue}
	<slot {currentValue}>
		{currentValue}
	</slot>
{/key}
