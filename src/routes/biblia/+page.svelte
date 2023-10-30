<script lang="ts">
	import { page } from '$app/stores';
	import { onMount } from 'svelte';

	import Navbar from '$lib/components/Navbar.svelte';
	import Versiculo from '$lib/components/Versiculo.svelte';

	let promise: any = null;

	async function getList() {
		const urlParams = $page.url.searchParams;
		const isVerso = urlParams?.has('verso');
		const verso = isVerso ? urlParams.get('verso') : 'João+3:16';
		const url = `https://bible-api.com/${verso}?translation=almeida`;

		await new Promise((r) => setTimeout(r, 1000)); // atraso intencional

		return await fetch(url)
			.then((r) => r.json())
			.then((data) => data);
	}

	onMount(() => {
		promise = getList();
	});
</script>

<body>
	<div class="hero" data-theme="dark">
		<Navbar />
	</div>

	<main class="container">
		<h1>Teste de API Pública</h1>

		{#await promise}
			<h3 aria-busy="true">Obtendo dados, aguarde…</h3>
		{:then data}
			<!-- {JSON.stringify(data)} -->
			<Versiculo {data} />
		{:catch error}
			<div class="error">
				Acesso aos dados não disponíveis no momento. Tente novamente, mais tarde.
				<p>{error}</p>
			</div>
		{/await}
	</main>
	<footer class="container">
		<small>
			<b> Exemplo de uso: </b>
			/apis?verso=1 Coríntios 13:4-7
		</small>
	</footer>
</body>

<style>
	div.error {
		color: var(--del-color);
	}
	div.error > * {
		color: var(--muted-color);
	}
</style>
