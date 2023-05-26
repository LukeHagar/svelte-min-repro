<script>
	// Docs
	import DocsShell from '$lib/DocsShell.svelte';

	// Components
	import Counter from '$lib/Counter.svelte';

	// Local
	const monthValues = [
		'January',
		'Feburary',
		'March',
		'April',
		'May',
		'June',
		'July',
		'August',
		'September',
		'October',
		'November',
		'December'
	];

	let index;
	let currentValue;
</script>

<Counter bind:index bind:currentValue values={monthValues} />

<DocsShell>
	<svelte:fragment slot="usage">
		<div>Current Value: {currentValue}</div>
		<div>Index: {index}</div>
	</svelte:fragment>
	<div>Current Value: {currentValue}</div>
	<div>Index: {index}</div>
</DocsShell>
