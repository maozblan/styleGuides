<script>
	import "@fontsource/anton";
	import "@fontsource/lato";
	let { hex, desc } = $props();

</script>

<button class="col" onclick={() => {
		navigator.clipboard.writeText(hex);
		alert(`Copied ${hex} to clipboard`);
	}}>
	<div id="color" style="background: #{hex}"></div>
	<p id="hex">#{hex}</p>
	<p>{desc}</p>
</button>

<style>
	* {
		font-family: "Lato", sans-serif;
		color: var(--text);
	}
	#hex {
		font-family: "Anton", sans-serif;
		font-size: 1.5em;
		margin-bottom: 0;
	}
	#color {
		width: 7rem;
		margin-top: 0.5rem;
		aspect-ratio: 1;
	}
	button {
		margin: 1rem;
		width: 8rem;
		height: 15rem;
		border: 1px solid var(--text);
		background-color: transparent;
		align-items: center;
		cursor: pointer;
		&:hover {
			border-color: var(--ac);
		}
	}
</style>
