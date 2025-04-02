<script lang="ts">
  import Img from "$lib/components/Img.svelte";
  import "@fontsource/lato";

  const imgs: ImgObj[] = [
    {
      id: "cf_star",
      desc: "star",
    },
    {
      id: "cf_plus",
      desc: "plus",
    },
    {
      id: "cf_minus",
      desc: "minus",
    },
  ];
</script>

<h1>click effects</h1>

<p>these are effects that popup when the user clicks onto anything. they are meant to be temporary so please make them simple.</p>
<p>if they are corresponding to an icon, they should be related to the icon.</p>

<br />

<p>requirements:</p>
<ul>
  <li>60 by 60px, with around 2-3 px of padding on all sides</li>
  <li>object should be relatively square and centered</li>
  <li>object shousld be outlined with a single 3px solid white outline, centered on path</li>
  <li>object should be simplistic and colored with one singular linear gradient with the color in bottom right-sih area and black in top leftish area.</li>
</ul>

<br />

<p>some examples</p>
<div class="row">
  {#each imgs as i (i)}
    <Img id={i.id} desc={i.desc} />
  {/each}
</div>

<style>
  * {
    font-family: "Lato", sans-serif;
  }
</style>
