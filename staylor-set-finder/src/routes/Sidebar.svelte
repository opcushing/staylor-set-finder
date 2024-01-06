<script>
	import ChordsDropdown from './Sidebar/ChordsDropdown.svelte';
</script>

<div class="content">
	<h1>List of Pitch Class Sets</h1>
	<!-- TODO: insert a clickable "MdMenu" icon. Collapses / uncollapses the menu on click. -->
	<ChordsDropdown />
</div>

<style>
	.content {
		width: 50%;
		text-align: center;
		background-color: lightgrey;
	}
</style>
