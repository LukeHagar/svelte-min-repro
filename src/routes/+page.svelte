<script lang="ts">
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

	let index: any;
	let indexValue: any;
</script>

<Counter bind:index bind:currentValue={indexValue} values={monthValues} />

<DocsShell>
	<svelte:fragment slot="usage">
		<div>Current Value: {indexValue}</div>
		<div>Index: {index}</div>
	</svelte:fragment>
	<div>Current Value: {indexValue}</div>
	<div>Index: {index}</div>
</DocsShell>
