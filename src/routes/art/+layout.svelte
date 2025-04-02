<script lang="ts">
  import { base } from "$app/paths";
	import { page } from "$app/state";
	import "@fontsource/anton";
	import "@fontsource/lato";

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
	div.everything-bagel {
		height: 100%;
		width: 100%;
		overflow: hidden;
	}
	h1 {
		font-family: "Anton", sans-serif;
	}
	p {
		font-family: "Lato", sans-serif;
	}
	#header {
		margin-bottom: 1rem;
		h1,
		p {
			text-align: center;
		}
	}
	#content {
		flex-grow: 1;
		height: 0;

		nav {
			width: 20%;
			height: 100%;
			a {
				color: var(--text);
				padding: 1rem 1rem;
				font-family: "Anton", sans-serif;
				font-stretch: expanded;
				letter-spacing: 0.1rem;
				text-align: left;
				text-decoration: none;
				&:hover,
				&:active {
					text-decoration: none;
					color: var(--ac);
				}
				&.active {
					color: var(--ac);
					text-align: right;
				}
			}
		}
		& > div {
			width: 80%;
			height: 100%;
			border-left: 0.5rem solid var(--ac);
			padding: 1rem;
			overflow: auto;
		}
	}
</style>
