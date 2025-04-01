<script lang=ts>
  import { img } from "$lib/img";
	import "@fontsource/lato";

	let { id, desc, size = 8 } = $props();
</script>

<div class="col" style="--s: {size}rem;">
	<img src={img[id as string]} alt={desc} />
	<p>{desc}</p>
</div>

<style>
	.col {
		margin: 1rem;
		align-items: center;
	}
	p {
		font-family: "Lato", sans-serif;
	}

	img {
		width: var(--s);
		height: auto;
		padding: 0.5rem;
		border: var(--text) 1px solid;
	}
</style>
