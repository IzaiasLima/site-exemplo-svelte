<script>
	import Navbar from '$lib/components/Navbar.svelte';
</script>

<body>
	<div class="hero" data-theme="dark">
		<Navbar />
	</div>

	<main class="container">
		<h1>Página de Teste</h1>

		<div class="grid">
			<section>
				<div>
					Lorem ipsum dolor sit amet consectetur adipisicing elit. Quasi in inventore dignissimos
					quis perspiciatis at fugit aliquid unde aperiam cupiditate maxime, voluptatem quam libero
					reprehenderit, rerum pariatur possimus natus corporis.
				</div>
			</section>
			<div>
				<button>Clique-me</button>
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
