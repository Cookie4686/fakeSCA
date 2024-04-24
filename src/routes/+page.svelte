<script>
	import Media from '../components/media.svelte';
</script>

<svelte:head>
	<title>SCA</title>
</svelte:head>

<main>
	<div class="logo flex justify-center">
		<img src="/src/public/SCAlogo2023.png" alt="SCA logo" draggable="false" class="select-none" />
	</div>
	<div class="flex flex-wrap justify-center gap-4">
		<p class="trademark text-center text-[1.5rem]">
			<span class="font-bold">โรงเรียนสามมุกคริสเตียนวิทยา</span>
			<br />
			<span>Sammuk Christian Academy</span>
		</p>
		<div class="inline-flex w-full justify-center gap-8">
			<a class="btn btn-1" href="/" target="_blank"><span>Photo Albums | ภาพกิจกรรม</span></a>
			<a class="btn btn-2" href="/home/"><span>Home Page | เข้าสู่เว็บไซต์</span></a>
		</div>
		<Media></Media>
	</div>
</main>

<style>
	main {
		min-height: 100vh;
		padding: 2.5% 2.5%;
		background: #1d2152 url(/src/public/bg.svg) no-repeat center bottom;
		background-size: cover;
		color: white;
	}
	main > div {
		padding: 1rem 0;
	}
	.logo {
		padding: 1.5rem 0 3rem 0;
	}
	.logo img {
		width: clamp(7.5rem, 20%, 12.5rem);
	}
	.btn {
		width: clamp(7.5rem, 33%, 15.5rem);
	}
	.btn span {
		white-space: nowrap;
		overflow: hidden;
		text-overflow: ellipsis;
	}
	.btn-1 {
		color: white;
		border-color: white;
		background-color: transparent;
	}
	.btn-2 {
		color: var(--blue);
		border-color: var(--lightblue);
	}
	.btn-2:hover,
	.btn-2:focus {
		border-color: white;
		background-color: var(--yellow);
	}

	/* Tablet */
	@media all and (min-width: 500px) {
		.trademark {
			font-size: 2rem;
		}
	}
	/* Desktop */
	@media all and (min-width: 768px) {
		.trademark {
			font-size: 2.25rem;
		}
	}
</style>
