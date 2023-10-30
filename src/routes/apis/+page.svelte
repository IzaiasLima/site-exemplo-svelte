<script lang="ts">
	import { onMount } from 'svelte';

	import Navbar from '$lib/components/Navbar.svelte';
	import Item from '$lib/components/Item.svelte';

	let promise: any = [];

	async function getList() {
		await new Promise((r) => setTimeout(r, 1000)); // atraso intencional
		return await fetch(`https://api.publicapis.org/entries`)
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
			<ul class="cards">
				<li>
					<h3>
						Total de APISs encontradas: {data.count}
					</h3>
				</li>
				{#each Object.values(data.entries) as item}
					<li>
						<Item {item} />
					</li>
				{/each}
			</ul>
		{:catch error}
			<div class="error">
				Acesso aos dados não disponíveis no momento. Tente novamente, mais tarde.
				<p>{error}</p>
			</div>
		{/await}
	</main>
</body>

<style>
	ul.cards {
		padding: 0;
	}

	ul.cards > li {
		list-style: none;
	}

	div.error {
		color: var(--del-color);
	}
	div.error > * {
		color: var(--muted-color);
	}
</style>
