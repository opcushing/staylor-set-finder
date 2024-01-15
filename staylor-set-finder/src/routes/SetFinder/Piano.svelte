<script>
	import Key from './Key.svelte';

	// collection of keys bound to a selection array.
</script>

<div class="keybed">
	<div class="keys">
		<Key />
		<Key number={2} />
		<Key number={4} />
		<Key number={5} />
		<Key number={7} />
		<Key number={9} />
		<Key number={11} />
	</div>
	<div class="keys blackKeys">
		<div class="side" />
		<Key isWhite={false} number={1} />
		<Key isWhite={false} number={3} />
		<div class="gap" />
		<Key isWhite={false} number={6} />
		<Key isWhite={false} number={8} />
		<Key isWhite={false} number={10} />
		<div class="side" />
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

		position: relative;
	}

	.keys {
		display: flex;
		flex-direction: row;
		padding: 1rem;
		width: auto;
		height: 100%;

		box-sizing: border-box;
		gap: 0.5rem;

		pointer-events: none;
	}

	.blackKeys {
		position: absolute;
		top: 0;
		left: 0;
		right: 0;
		bottom: 0;
	}

	.gap {
		width: 100%;
	}

	.side {
		width: 50%;
	}
</style>
