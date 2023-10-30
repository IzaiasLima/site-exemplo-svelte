<script lang="ts">
	import Sun from '$lib/icons/Sun.svelte';
	import Moon from '$lib/icons/Moon.svelte';

	let isDark: boolean;

	function toggleTheme() {
		const elem = document.documentElement;
		isDark = elem.getAttribute('data-theme') === 'dark';
		elem.setAttribute('data-theme', isDark ? 'light' : 'dark');
		isDark = !isDark;
	}
</script>

<button on:click={toggleTheme} data-tooltip="Cor do tema" data-placement="left">
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
