<script>
	import Media from '../components/media.svelte';
	import { base } from '$app/paths';
	import logo from '$lib/assets/SCAlogo2023.png'
</script>

<svelte:head>
	<title>Sammuk Christian Academy</title>
</svelte:head>

<main>
	<div class="flex justify-center">
		<div class="logo flex justify-center items-center">
			<img src={logo} alt="SCA logo" draggable="false" class="select-none" />
		</div>
	</div>
	<div class="flex justify-center">
		<div class="trademark text-center">
			<p class="trademark-th">โรงเรียนสามมุกคริสเตียนวิทยา</p>
			<p class="trademark-en">Sammuk Christian Academy</p>
		</div>
	</div>
	<div class="flex justify-center">
		<div class="btn-container inline-flex justify-center">
			<a class="btn btn-1" href="{base}/" target="_blank"><span>Photo Albums | ภาพกิจกรรม</span></a>
			<a class="btn btn-2" href="{base}/home/"><span>Home Page | เข้าสู่เว็บไซต์</span></a>
		</div>
	</div>
	<Media></Media>
</main>

<style>
	main {
		min-height: 100vh;
		padding-top: 5vh;
		background: #1d2152 url(/src/lib/assets/bg.svg) no-repeat center bottom;
		background-size: cover;
		color: white;
	}
	img {
		height: 20vh;
		object-fit: contain;
		/* width: clamp(7.5rem, 30%, 15rem); */
	}
	.logo {
		margin-bottom: 5vh;
		/* min-height: 20vh; */
	}
	.trademark {
		--th-size: 1.5rem;
		--en-size: calc(var(--th-size) * 0.8); 
		margin-bottom: 15vh;
	}
	.trademark-th {
		font-size: var(--th-size);
		font-weight: 600;
		margin-bottom: calc(var(--th-size) * 0.25);
	}
	.trademark-en {
		font-size: var(--en-size);
		font-family: Satisfy;
	}
	.btn-container {
		width: 100vw;
		padding: 0 0.5rem;
		justify-content: center;
		gap: 3rem;
		margin-bottom: 15vh;
	}
	
	/* Tablet */
	@media all and (min-width: 550px) {
		main {
			padding-top: 7.5vh;
		}
		img {
			height: 22.5vh;
		}
		.logo {
			margin-bottom: 10vh;
		}
		.trademark {
			--th-size: 2.75rem;
			margin-bottom: 15vh;
		}
		.btn-container {
			margin-bottom: 5vh;
		}
	}
	/* Desktop */
	@media all and (min-width: 1050px) {
		main {
			padding-top: 7.5vh;
		}
		img {
			height: 25vh;
		}
		.logo {
			margin-bottom: 7.5vh;
		}
		.trademark {
			--th-size: 3rem;
			margin-bottom: 12.5vh;
		}
	}
	
	.btn {
		width: clamp(9rem, 33vw, 18rem);
		height: clamp(3rem, 3vh, 6rem);
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
</style>
