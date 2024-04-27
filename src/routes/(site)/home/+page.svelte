<script>
	import Slider from "../../../components/slider.svelte";
</script>

<svelte:head>
	<title>Home</title>
</svelte:head>

<div class="page">
	<!-- <header class="flex flex-wrap justify-center">
	</header> -->
	
	<main>
		<!-- <Slider></Slider> -->
		<!-- <section class="announcement">
			<div class="topic">
				<h2>Announcement</h2>
			</div>
		</section>
	
		<section class="achievement">
		</section> -->
		
		<section class="information">
			<h2>Life in SCA</h2>
			<div>
				<button>ข้อมูลทั่วไป</button>
				<button>Facilities</button>
			</div>
		</section>
	
		<section class="admission">
			<h2>Admission</h2>
			<div>
				<button>ทุนการศึกษา</button>
			</div>
		</section>
	
	
		<section class="maps">
			<h2>แผนที่โรงเรียน</h2>
		</section>
	</main>

</div>

<style>
	.page {
    padding-top: var(--navheight);
  }
	header {
		padding-top: 0;
		min-height: 100vh;
	}
	section {
		padding-bottom: 2.5rem;
	}
	section h2 {
		color: var(--blue);
		text-align: center;
		padding: 1rem 0;
		font-size: 1.5rem;
		font-weight: 600;
	}
</style>
