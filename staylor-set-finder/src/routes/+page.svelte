<script>
	import SetFinder from './SetFinder.svelte';
	import Sidebar from './Sidebar.svelte';
</script>

<div class="app">
	<Sidebar />
	<SetFinder />
</div>

<style>
	.app {
		display: flex;
		flex-direction: row;
		min-height: 100vh;
	}
</style>
