<script>
	import Media from './media.svelte';
</script>

<footer class="min-h-40 w-full py-8">
	<ul>
		<li class="link select-none">
			<a href="/">Home</a>
			<a href="/about/">About</a>
			<a href="/">Contact</a>
			<a href="/">Donate</a>
			<a href="/">Student Council</a>
			<a href="/">Albums</a>
			<a href="/">Admission</a>
		</li>
	</ul>

	<div class="contact pt-12">
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

	.link a {
		padding: 0 1.5rem;
	}
</style>
