<script>
  import Modal from "./Modal.svelte";

  let showModal = false;
</script>

<style>
  .input {
    font-style: italic;
    opacity: 50%;
    width: 50%;
  }
</style>

<button on:click={() => (showModal = true)}>Forgot Password?</button>

{#if showModal}
  <Modal on:close={() => (showModal = false)}>
    <h2>Did you forget your password?</h2>
    <p>Enter your email below to reset your password.</p>
    <input class="input" placeholder="Email" required />
  </Modal>
{/if}
