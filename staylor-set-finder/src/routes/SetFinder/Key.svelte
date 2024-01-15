<script>
	export let number = 0;
	export let selected = false;
	export let isWhite = true;

	function toggleSelect() {
		selected = !selected;
	}
</script>

<button class:white={isWhite} class:black={!isWhite} class:selected on:click={toggleSelect}>
	<h1>{number}</h1>
</button>

<style>
	button {
		width: 100%;
		height: 100%;
		border: solid;
		border-width: 5px;
		border-top-left-radius: 3px;
		border-top-right-radius: 3px;
		border-bottom-left-radius: 20px;
		border-bottom-right-radius: 20px;
		display: block;
		position: relative;
		box-sizing: border-box;

		pointer-events: all;
	}

	h1 {
		position: absolute;
		bottom: 0;
		right: 0;
		left: 0;
		text-align: center;
		user-select: none;
	}

	.white {
		background-color: white;
		border-color: black;
		color: black;
	}

	.black {
		background-color: black;
		border-color: gray;
		color: white;
		height: 60%;
	}

	.white:hover:not(.selected) {
		background-color: #dcdcdc;
	}
	.black:hover:not(.selected) {
		background-color: #3f3f3f;
	}

	.selected {
		background-color: hsl(197, 90%, 65%);
		border-color: black;
		color: black;
	}

	.selected:hover {
		background-color: hsl(197, 91%, 56%);
	}
</style>
