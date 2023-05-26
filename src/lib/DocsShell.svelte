<script>
	// Docs
	import LayoutPage from './LayoutPage.svelte';
</script>

<LayoutPage>
	<slot name="usage">(usage)</slot>
</LayoutPage>

<slot>(default)</slot>
