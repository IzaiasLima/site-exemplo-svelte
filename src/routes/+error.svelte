<script lang="ts">
  import { page } from "$app/stores";
  import Navbar from "$lib/components/Navbar.svelte";
</script>

<body>
  <Navbar />

  <main class="container">
    <h1>{$page.status}: {$page.error?.message}</h1>

    <div>
      <p>Parece que tivemos um probleminha aqui.</p>
      <p>A página que você tentou acessar não existe.</p>
      <p>Favor verificar e tentar novamente.</p>
      <a role="button" href="/">Voltar para a página inicial</a>
    </div>
  </main>
</body>

<style>
  main {
    text-align: center;
  }
  p {
    margin: 0;
    padding: 0;
    font-size: 1.5rem;
    font-weight: 300;
  }
  h1 {
    color: var(--muted-color);
    font-size: 3rem;
  }
  a {
    margin-top: 3rem;
  }
</style>
