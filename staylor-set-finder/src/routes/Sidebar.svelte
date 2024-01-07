<script>
	import Menu from 'svelte-material-icons/Menu.svelte';
	import { fly, slide } from 'svelte/transition';

	import ChordsDropdown from './Sidebar/ChordsDropdown.svelte';

	let open = true;

	function ToggleSidebar() {
		open = !open;
	}
</script>

<div class="sidebar">
	{#if open}
		<div class="content">
			<h1>List of Pitch Class Sets</h1>
			<ChordsDropdown />
		</div>
	{/if}
	<!-- TODO: insert a clickable "MdMenu" icon. Collapses / uncollapses the menu on click. -->
	<button class="toggle" on:click={ToggleSidebar}>
		<Menu size="2rem" />
	</button>
</div>

<style>
	h1 {
		margin: 0;
		text-wrap: nowrap;
	}

	.sidebar {
		width: fit-content;
		background-color: lightgrey;
		display: flex;
		flex-direction: row;
	}

	.content {
		padding: 0.67em;
		gap: 1rem;
	}

	.toggle {
		align-self: flex-start;
		margin-top: 1em;
		cursor: pointer;
		border: none;
		background: none;
	}
</style>
