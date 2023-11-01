<script>
  import Toggle from "$lib/components/Toggle.svelte";
</script>

<div class="header">
  <!-- Logo -->
  <a href="/" class="logo">LOUTTAINE</a>

  <!-- Icon show/hide menu -->
  <input class="side-menu" type="checkbox" id="side-menu" />
  <label class="icon" for="side-menu"><span class="icon-line" /></label>

  <!-- Menu -->
  <nav class="nav">
    <ul class="menu">
      <li><a href="/teste" class="contrast">Erro 404</a></li>
      <li><a href="/article" class="contrast">Article</a></li>
      <li><a href="/apis" class="contrast">API</a></li>
      <li><a href="/biblia" class="contrast">Bíblia</a></li>
      <li><a href="/dialog" class="contrast">Dialog</a></li>

      <!-- Change theme color -->
      <li><Toggle /></li>
    </ul>
  </nav>
</div>

<style>
  :root {
    --menu-bg-color: rgba(0, 0, 0, 0.7);
  }
  .header {
    padding: 0;
    top: 0;
    position: sticky;
    width: 100%;
    box-shadow: 1px 1px 5px 0px var(--secondary);
    background-color: var(--menu-bg-color);
  }
  .logo {
    display: inline-block;
    margin-left: 10px;
    padding-left: 7px;
    color: var(--primary);
    font-size: 2em;
    font-weight: 600;
    text-shadow: 2px 2px 2px rgba(0, 0, 0, 0.4);
  }
  .nav {
    position: fixed;
    width: 100%;
    /* max-height: none; */
    background-color: var(--menu-bg-color);
    overflow: hidden;
  }

  .nav {
    max-height: 0;
    transition: max-height 0.5s ease-out;
  }

  ul.menu {
    align-items: start;
    padding: 0;
    padding-right: 20px;
    list-style: none;
    flex-direction: column;
  }

  .menu li {
    padding-top: 5px;
  }
  .menu li:first-child {
    padding-top: 20px;
  }

  .menu li:last-child {
    margin-left: 20px;
  }

  .menu a {
    display: block;
    margin-left: 10px;
    color: var(--primary-inverse);
  }

  .menu a:hover {
    background-color: var(--secondary);
  }

  .icon {
    cursor: pointer;
    float: right;
    padding: 23px 20px;
  }

  .icon-line {
    background: var(--primary-inverse);
    display: block;
    height: 2px;
    position: relative;
    width: 24px;
  }

  .icon-line::before,
  .icon-line::after {
    content: "";
    position: absolute;
    display: block;
    width: 100%;
    height: 100%;
    background: var(--primary-inverse);
    transition: all 0.2s ease-out;
  }

  .icon-line::before {
    top: 5px;
  }

  .icon-line::after {
    top: -5px;
  }

  .side-menu {
    display: none;
  }

  .side-menu:checked ~ nav {
    max-height: 100vh;
  }

  .side-menu:checked ~ .icon .icon-line {
    background: transparent;
  }

  .side-menu:checked ~ .icon .icon-line::before {
    top: 0;
    transform: rotate(-45deg);
  }

  .side-menu:checked ~ .icon .icon-line::after {
    top: 0;
    transform: rotate(45deg);
  }

  @media (min-width: 768px) {
    .nav {
      position: relative;
      top: 0;
      float: right;
      max-height: none;
      width: fit-content;
      background-color: transparent;
    }

    ul.menu {
      flex-direction: row;
    }

    .menu li,
    .menu li:first-child {
      float: left;
      padding-top: 15px;
    }

    .menu a:hover {
      background-color: transparent;
      color: var(--primary);
    }

    .icon {
      display: none;
    }
  }
</style>
