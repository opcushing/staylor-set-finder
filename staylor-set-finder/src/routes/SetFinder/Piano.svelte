<script>
	import Key from './Key.svelte';

	// collection of keys bound to a selection array.
</script>

<div class="keybed">
	<div class="whiteKeys">
		<Key isWhite={true} />
		<Key isWhite={true} number={2} />
		<Key isWhite={true} number={4} />
		<Key isWhite={true} number={5} />
		<Key isWhite={true} number={7} />
		<Key isWhite={true} number={9} />
		<Key isWhite={true} number={11} />
	</div>
</div>

<style>
	.keybed {
		background-color: lightgrey;
		border-color: black;
		border: solid;
		border-width: 5px;
		border-radius: 20px;
		width: 860px;
		height: 360px;
		box-sizing: border-box;
	}

	.whiteKeys {
		display: flex;
		flex-direction: row;
		justify-content: space-evenly;
		align-items: center;
		padding: 1rem;
		width: auto;
		height: 100%;

		box-sizing: border-box;
		gap: 0.5rem;
	}
</style>
