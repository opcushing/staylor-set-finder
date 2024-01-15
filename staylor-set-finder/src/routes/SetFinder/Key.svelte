<script>
	export let number = 0;
	export let selected = false;
	export let isWhite = true;
</script>

<div class:white={isWhite} class:black={!isWhite}>
	<h1>{number}</h1>
</div>

<style>
	div {
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
	}

	h1 {
		position: absolute;
		bottom: 0;
		right: 0;
		left: 0;
		text-align: center;
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
</style>
