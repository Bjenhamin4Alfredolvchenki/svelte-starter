<script>
  import Scrolly from "$components/helpers/Scrolly.svelte";
  let value;
</script>

<section id="scrolly">
  <h2 style="position: sticky; top: 4em;">Scrolly <span>{value}</span></h2>
  <div class="spacer" />
  <Scrolly bind:value>
    {#each [0, 1, 2, 3, 4] as text, i}
      <div class="step" class:active={value === i}>
        <p>{text}</p>
      </div>
    {/each}
  </Scrolly>
  <div class="spacer" />
</section>

<style>
  .spacer {
    height: 75vh;
  }

  .step {
    height: 80vh;
    background: var(--color-gray-100);
    text-align: center;
  }

  .step p {
    padding: 1rem;
  }
</style>
