<script lang="ts">
	import { page } from '$app/stores';
	import Navbar from '$lib/components/Navbar.svelte';
</script>

<body>
	<div class="hero" data-theme="dark">
		<Navbar />
	</div>

	<main class="container">
		<h1>{$page.status}: {$page.error?.message}</h1>

		<div class="grid">
			<h3>Parece que tivemos um probleminha aqui...</h3>
			<div>
				<a role="button" href="/">Voltar para a página inicial</a>
			</div>
		</div>
	</main>
	<!-- Footer -->
	<footer class="container">
		<small
			>Built with <a href="https://picocss.com">Pico</a> •
			<a href="https://github.com/picocss/examples/tree/master/v1-company/">Source code</a></small
		>
	</footer>
	<!-- ./ Footer -->
</body>
