<script>
	import Media from './media.svelte';
</script>

<footer class="min-h-40 w-full py-8">
	<div class="contact">
		<p class="font-bold text-xl">Contact Us</p>
		<div class="py-4">
			<Media></Media>
		</div>
		<div class="pt-4 text-sm">
			<p class="text-base font-bold">Sammuk Christian Academy</p>
			<p>166 Bangsane-Angsila Road, Sansuk Sub-district, Muang District, Chonburi, 20130</p>
			<p>Tel: 081-432-9799 | 038-398-316</p>
			<br />
			<p>officer@sca.ac.th</p>
		</div>
	</div>
</footer>

<style>
	footer {
		color: var(--primary);
		background-color: var(--primary-opposite);
		text-align: center;
	}
</style>
