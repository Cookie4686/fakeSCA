<script>
  import Nav from "../../../components/nav.svelte";
	import Media from "../../../components/media.svelte";
</script>

<svelte:head>
	<title>Contact</title>
</svelte:head>

<div class="site">
  <Nav></Nav>
  <div class="page">
    <header class="flex flex-wrap justify-center items-center">
      <h1>ติดต่อเรา</h1>
    </header>
    <main>
      <section>
        <h2>ช่องทางออนไลน์</h2>
        <div>
          <p>อีเมล์: officer@sca.ac.th</p>
          <p>โทรศัพท์: 081-432-9799 | 038-398-316</p>
          <div class="pt-8">
            <Media></Media>
          </div>
        </div>
      </section>
      <section>
        <h2>ติดต่อธุรการ</h2>
        <div>
          <p>จันทร์-เสาร์ | 8:00-17:00 น.</p>
          <p>* ปิดทำการวันอาทิตย์และทุกวันหยุดนักขัตฤกษ์</p>
        </div>
        <div class="pt-4">
          <p>166 ถนน บางแสน-อ่างศิลา ตำบลแสนสุข อำเภอเมืองชลบุรี ชลบุรี 20130</p>
        </div>
      </section>
    </main>
  </div>
</div>

<style>
	.site {
		min-height: 100dvh;
		display: grid;
		grid-template-rows: 1fr;
		grid-template-columns: minmax(0, 1fr);
	}
	.page {
		--navheight: 5rem;
    position: relative;
	}
  .page::after {
    content: '';
    position: absolute;
    inset: 0;
    width: 100%;
    height: 100%;
    z-index: -1;
    background: url(/src/lib/assets/contact/bg_contact.webp) no-repeat center center;
    background-size: cover;
    opacity: 0.15;
  }
  header {
    min-height: 40vh;
    padding-top: var(--navheight);
  }
  header h1 {
    font-size: 2.5rem;
    font-weight: 600;
  }
</style>