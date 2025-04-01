<script lang="ts">
	import "@fontsource/lato";
	import Color from "$lib/components/Color.svelte";

	const colors: ColorObj[] = [
		{
			hex: "ffffff",
			desc: "white",
		},
		{
			hex: "7bdbe8",
			desc: "blue accent",
		},
		{
			hex: "226a74",
			desc: "dark blue",
		},
		{
			hex: "f2c144",
			desc: "orange / coin",
		},
		{
			hex: "a66223",
			desc: "coffee",
		},
		{
			hex: "c4f279",
			desc: "green",
		},
		{
			hex: "92cc33",
			desc: "dark green",
		},
		{
			hex: "4cd649",
			desc: "click effect green",
		},
		{
			hex: "fa2828",
			desc: "click effect red",
		},
	];
	const bgs: ColorObj[] = [
		{
			hex: "111111",
			desc: "main",
		},
		{
			hex: "1a1a1a",
			desc: "sub",
		},
		{
			hex: "333333",
			desc: "buttons",
		},
	];
</script>

<h1>color color color</h1>

<p>
	since there are no lines, colors will be what differentiates one part of an
	item from another.
</p>
<p>
	feel free to use gradients (don't over use them) here and there for more
	flair. also feel free to create a slight variant of any of the preexisitng
	palette to use and REUSE. unless it is an accent for a specific purpose, do
	not create one time use colors.
</p>
<p>
	feel free to use transparency in parts of your image. and even gradients to
	transparent.
</p>
<p>
	semi transparent parts are usually 50% or 70% opacity. don't go overboard.
</p>

<br />

<p>for all colors, please make it bright with medium to high saturation.</p>
<p>
	also do check that contrast is high enough for the image to be recognizable in
	black in white.
</p>

<br />

<p>below is our current list of colors. click to copy hex code.</p>

<div class="colors row">
	{#each colors as c (c)}
		<Color hex={c.hex} desc={c.desc} />
	{/each}
</div>

<p>
	below is the possible background colors of the images if you want to test
	them.
</p>

<div class="colors row">
	{#each bgs as b (b)}
		<Color hex={b.hex} desc={b.desc} />
	{/each}
</div>

<style>
	* {
		font-family: "Lato", sans-serif;
	}
	.colors {
		flex-wrap: wrap;
	}
</style>
