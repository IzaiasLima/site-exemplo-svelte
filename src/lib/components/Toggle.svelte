<script lang="ts">
  import Sun from "$lib/icons/Sun.svelte";
  import Moon from "$lib/icons/Moon.svelte";

  let isDark: boolean;

  function toggleTheme() {
    const elem = document.documentElement;
    isDark = elem.getAttribute("data-theme") === "dark";
    elem.setAttribute("data-theme", isDark ? "light" : "dark");
  }

  function showTooltip() {
    const tooltip = document.getElementById("theme");
    tooltip?.setAttribute("data-tooltip", "Alterar a cor do tema");
  }

  function hideTooltip() {
    const tooltip = document.getElementById("theme");
    tooltip?.removeAttribute("data-tooltip");
  }
</script>

<button
  id="theme"
  on:click={toggleTheme}
  on:mouseenter={showTooltip}
  on:mouseleave={hideTooltip}
  data-placement="left"
  data-tooltip="Cor do tema"
>
  {#if isDark}
    <Sun />
  {:else}
    <Moon />
  {/if}
</button>

<style>
  button {
    background-color: transparent;
    padding: 0 15px;
  }

  button:hover {
    border-color: var(--muted-color);
  }
</style>
