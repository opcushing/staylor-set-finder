<script>
	import Menu from 'svelte-material-icons/Menu.svelte';
	import { fly, slide } from 'svelte/transition';
	import { cubicOut } from 'svelte/easing';
	import { tweened } from 'svelte/motion';

	import ChordsDropdown from './Sidebar/ChordsDropdown.svelte';

	let visible = true;
</script>

<div class="sidebar">
	{#if visible}
		<div in:slide={{ axis: 'x', duration: 400 }} out:slide={{ axis: 'x', duration: 400 }}>
			<div class="content">
				<h1>List of Pitch Class Sets</h1>
				<ChordsDropdown />
			</div>
		</div>
	{/if}
	<button
		class="toggle"
		on:click={() => {
			visible = !visible;
		}}
	>
		<Menu size="2rem" />
	</button>
</div>

<style>
	h1 {
		margin: 0;
		text-wrap: nowrap;
	}

	.sidebar {
		width: auto;
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
