<script lang="ts">
	export let data: any;
	let hasData: boolean = !(data === null || data.error);
</script>

<article>
	<header>
		<h2>
			{#if hasData}
				{data?.reference}
			{:else}
				Referência inexistente!
			{/if}
		</h2>
	</header>

	<!-- {JSON.stringify(data)} -->

	<div>
		{#if hasData && data.verses != undefined}
			{#each Object.values(data.verses) as verso}
				<h3>{verso.verse}. {verso.text.trim()}</h3>
			{/each}
		{:else}
			<h3>
				Por favor, revise sua solicitação. Parece que a referência que você passou não existe ou foi
				informada incorretamente.
			</h3>
		{/if}
	</div>
</article>

<style>
	header > h2 {
		font-weight: 400;
	}
</style>
