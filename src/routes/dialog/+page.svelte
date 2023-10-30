<script lang="ts">
	import Navbar from '$lib/components/Navbar.svelte';
	import Dialog from '$lib/components/Dialog.svelte';

	let dialog: any;
	let isConfirmado = false;

	function submit() {
		isConfirmado = true;
		dialog.close();
	}
</script>

<body>
	<div class="hero" data-theme="dark">
		<Navbar />
	</div>

	<main class="container">
		<h1>Modal</h1>

		<button on:click={() => dialog.showModal()} disabled={isConfirmado}>
			Solicitar Confirmação
		</button>

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
