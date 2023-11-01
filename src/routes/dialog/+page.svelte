<script lang="ts">
  import Navbar from "$lib/components/Navbar.svelte";
  import Dialog from "$lib/components/Dialog.svelte";

  let dialog: any;
  let isConfirmado = false;

  function submit() {
    isConfirmado = true;
    dialog.close();
  }
</script>

<body>
  <Navbar />

  <main class="container">
    <h1>Modal</h1>

    <div class="grid">
      <p>
        Clique no botão de confirmação para testar a funcionalidade do <i>
          diálogo modal.
        </i>
      </p>
      <button on:click={() => dialog.showModal()} disabled={isConfirmado}>
        Confirmar
      </button>
    </div>

    <hr />

    <Dialog
      onSubmit={submit}
      bind:dialog
      title="Confirme a sua concordância!"
      message="Ao clicar no botão 'Confirmar', abaixo, 
			você estará concordando com a nossa proposta."
    />

    {#if isConfirmado}
      <footer class="container">
        <h3>Usuário confirmou a operação.</h3>
      </footer>
    {:else}
      <h3 class="negado">Usuário não confirmou a operação.</h3>
    {/if}
  </main>
</body>

<style>
  h3.negado {
    color: var(--del-color);
  }
</style>
