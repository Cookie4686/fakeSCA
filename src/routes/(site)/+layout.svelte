<script>
	import Nav from '../../components/nav.svelte';
	import Footer from '../../components/footer.svelte';
</script>

<div class="site">
	<Nav></Nav>
	<div class="page"><slot /></div>
	<Footer></Footer>
</div>

<style>
	.site {
		min-height: 100dvh;
		display: grid;
		grid-template-rows: 1fr auto;
		grid-template-columns: minmax(0, 1fr);
	}

	.page {
		padding-top: 5rem;
		padding-left: 2rem;
		padding-right: 2rem;
	}
</style>
