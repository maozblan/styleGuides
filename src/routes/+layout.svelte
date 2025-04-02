<script lang="ts">
  import { base } from "$app/paths";
  import { page } from "$app/state";
  import "@fontsource/anton";
  import "@fontsource/lato";

  let { children } = $props();

  const pages: string[] = ["art"];
  console.log(page.url.pathname, base);
</script>

{#key page.url.pathname}
  {#if [`${base}`, "/"].includes(page.url.pathname)}
		 <div class="col everything-bagel">

    <h1>style guides for galactic coffee shop</h1>
    <p>mostly a hub to collect style guides in one place</p>
    <br />

    <div class="row">
      {#each pages as p (p)}
        <a href="{base}/{p}">
          <button>{p}</button>
        </a>
      {/each}
    </div>

		 </div>
  {:else}
    {@render children()}
  {/if}
{/key}

<style>
	 .everything-bagel {
		height: 100%;
		width: 100%;
		justify-content: center;
		align-items: center;
		overflow: hidden;
	}
  h1 {
    font-family: "Anton", sans-serif;
  }
  * {
    font-family: "Lato", sans-serif;
  }
  button {
    cursor: pointer;
    padding: 0.5rem;
    background-color: transparent;
    color: var(--text);
    border: 1px solid var(--text);
    &:hover {
      border-color: var(--ac);
      color: var(--ac);
    }
  }
</style>
