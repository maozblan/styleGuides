<script lang="ts">
  import { base } from "$app/paths";
	import { page } from "$app/state";

	const pages: string[] = [
		"start",
		"color",
		"effects",
		"items",
		"characters",
		"buildings",
		"splashes",
	];

	let { children } = $props();
</script>

<div class="col everything-bagel">
	<div id="header">
		<h1>art guide for galactic coffee shop</h1>
		<p>tl;dr - make it simple and blocky with minimal colors and no lines</p>
	</div>

	<div id="content" class="row">
		<nav class="col">
			{#each pages as p (p)}
				<a href="{base}/art/{p}" class:active={page.url.pathname === `${base}/art/${p}`}>{p}</a>
			{/each}
		</nav>
		<div class="col">
			{@render children()}
		</div>
	</div>
</div>

<style>
</style>
