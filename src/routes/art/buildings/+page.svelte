<script lang="ts">
	import Img from "$lib/components/Img.svelte";
	import "@fontsource/lato";

	const imgs: ImgObj[] = [
		{
			id: "cfs_1",
			desc: "coffee stand",
		},
		{
			id: "cfs_2",
			desc: "coffee shop top",
		},
		{
			id: "cfs_3",
			desc: "coffee shop bottom",
		},
	];
</script>

<h1>building buildings</h1>

<p>
	buildings are a hard topic as they have more of a distinct style that you will
	have to follow or create. buildings differ by region and their architecture
	style should be distinctly noticable.
</p>
<p>
	for now, the only buildings needed are the different coffee shops and stands.
	there is going to be changes to how the buildings are handled but for now,
	just follow the references.
</p>

<br />

<p>requirements:</p>
<ul>
	<li>all coffee shops/stands should be drawn at 500x500px</li>
	<li>
		all coffee shops/stands should have the cashier location centered around the
		same area
	</li>
	<li>should be stylized to fit the planet/area</li>
</ul>

<br />

<p>here are some examples for the current stage of buildings:</p>
<div class="row">
	{#each imgs as i (i.id)}
		<Img id={i.id} desc={i.desc} size={20} />
	{/each}
</div>
<p>things to note:</p>
<ul>
	<li>DO NOT add the coffee to your buildings, thank you</li>
	<li>the cashier area is similar for the shop and the stand</li>
	<li>
		the shop the broken into multiple parts depends on if the player character
		should be layered on top or below the sprite (can also be broken into parts
		for animation purposes)
	</li>
	<li>regardless of actual building size, the sprite is 500x500px</li>
	<li>
		buildings are clearly related with similar aspects such as: the blue/white
		lines, the green table with sharp and round corners, the yellow banner
	</li>
	<li>no use of gradients except for to transparent</li>
</ul>

<style>
	* {
		font-family: "Lato", sans-serif;
	}
</style>
