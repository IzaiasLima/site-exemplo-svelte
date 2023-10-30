<script lang="ts">
	export let dialog: {
		showModal(): any;
		close(): any;
	};
	export let title: string = '';
	export let message: string = '';
	export let onSubmit: any;

	$: () => onSubmit();
</script>

<dialog bind:this={dialog}>
	<dialog open>
		<article>
			<header>
				<a href="#close" on:click={dialog.close()} aria-label="Close" class="close" />
				<h3>{title}</h3>
			</header>
			<p>{message}</p>
			<footer>
				<a on:click={() => dialog.close()} href="#cancel" role="button" class="secondary">
					Cancelar
				</a>
				<a on:click={() => onSubmit()} href="#confirm" role="button"> Confirmar </a>
			</footer>
		</article>
	</dialog>
</dialog>
