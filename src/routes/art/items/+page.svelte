<script lang="ts">
	import Img from "$lib/components/Img.svelte";
	import "@fontsource/lato";
</script>

<h1>items and icons</h1>

<p>
	this is a list of all the things that should be used near text. style should
	be a slightly simplier version of how characters are drawn.
</p>
<p>
	items are icons are usually one in the same though icons tend to be displayed
	smaller.
</p>

<br />

<p>requirements:</p>
<ul>
	<li>100x100px or 150x150px unless specified otherwise</li>
	<li>only use solid block colors with minimal gradients</li>
	<li>easily recognizable at a glance (unique enough silhouettes)</li>
	<li>simple designs but leave enough room for variation such as upgrades</li>
	<li>NO use of path outlines unless specified otherwise</li>
</ul>

<br />

<p>
	below is the only item we have in game so far and a bit unconventional due to
	placement location and sizing. however, it's a good reference for item/icon
	simplicity and allowance for variation (the sleeve or the coffee can be
	colored differently).
</p>
<div class="row">
	<Img id="coffee" desc="coffee" size={6} />
</div>

<style>
	* {
		font-family: "Lato", sans-serif;
	}
</style>
