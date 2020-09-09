<script>
  let loading = false;
  function clicked() {
    loading = true;
    setTimeout(() => {
      loading = false;
    }, 10000);
  }
</script>

<style>
    .orange {
        background-color: #ff5a1f;
        color: white;
    }
    .orange:hover {
        background-color: #ff5a1f;
        color: white;
    }
</style>

<div class="outer-box">
  {#if loading == false}
    <button on:click={clicked} class="btn orange">LOGIN</button>
  {:else}
    <button class="btn orange">
      <span class="spinner-border spinner-border-sm" /> Loading..
    </button>
  {/if}
</div>
