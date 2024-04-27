<script>
	import Nav from '../../components/nav.svelte';
	import Footer from '../../components/footer.svelte';
</script>

<div class="site">
	<Nav></Nav>
	<slot />
	<Footer></Footer>
</div>

<style>
	.site {
		min-height: 100dvh;
		display: grid;
		grid-template-rows: 1fr auto;
		grid-template-columns: minmax(0, 1fr);
		--navheight: 5rem;
	}
</style>
