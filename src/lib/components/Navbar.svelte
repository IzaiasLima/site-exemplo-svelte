<script>
	import Toggle from '$lib/components/Toggle.svelte';
</script>

<nav class="container-fluid">
	<ul>
		<li>
			<a href="/" class="contrast"><strong>Brand</strong></a>
		</li>
	</ul>
	<ul>
		<li>
			<a href="/teste" class="contrast">Testar</a>
		</li>
		<li>
			<a href="/responsive" class="contrast">Responsivo</a>
		</li>
		<li>
			<a href="/apis" class="contrast">API</a>
		</li>
		<li>
			<a href="/biblia" class="contrast">Bíblia</a>
		</li>
		<li>
			<a href="/dialog" class="contrast">Dialog</a>
		</li>
		<li>
			<Toggle />
		</li>
	</ul>
</nav>
