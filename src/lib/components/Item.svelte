<script lang="ts">
	export let item: any;
</script>

<article>
	<header>
		<h2>API: {item.API}</h2>
		<p>{item.Description}</p>
	</header>
	<div>
		<p>Description: {item.Description}</p>
		<p>Category: {item.Category}</p>
		<p>Auth: {item.Auth}</p>
		<p>HTTPS: {item.HTTPS}</p>
		<p>Cors: {item.Cors}</p>
		<a target="_blank" href={item.Link}>{item.Link}</a>
	</div>
</article>

<style>
	header > p,
	div > p {
		font-size: 1.3em;
		font-weight: 200;
	}

	div > p {
		padding: 0;
		margin-bottom: 0.3em;
	}
	h2 {
		margin: 0;
	}
</style>
