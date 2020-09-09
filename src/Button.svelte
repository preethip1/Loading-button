<script>
  let loading = false;
  function clicked() {
    loading = true;
    setTimeout(() => {
      loading = false;
    }, 10000);
  }
</script>

<div class="outer-box">
  {#if loading == false}
    <button on:click={clicked} class="btn btn-primary">LOGIN</button>
  {:else}
    <button class="btn btn-primary">
      <span class="spinner-border spinner-border-sm" /> Loading..
    </button>
  {/if}
</div>
