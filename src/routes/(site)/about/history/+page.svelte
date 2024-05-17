<svelte:head>
  <title>School History</title>
</svelte:head>

<div class="page">
  <header class="flex flex-col justify-start items-center text-center">
    <div class="absolute top-1/2">
      <h1>ประวัติโรงเรียน</h1>
    </div>
  </header>
  <main>
    <section>
      <p>วันที่ 9 มกราคม ค.ศ. 1961 คณะกรรมการเตรียมการ 15 ท่าน ซึ่งได้รับการแต่งตั้งจากคณะธรรมกิจ เพื่อพิจารณาปัญหาการจัดตั้งโรงเรียน สำหรับแบบอาคารเรียนทางคณะกรรมการตัดสินใจรับเอาแบบของกระทรวงศึกษาธิการ แต่เนื่องจากปัญหาทางการเงิน ทำให้การเปิดโรงเรียนล่าช้าออกไป 1 ปี เป็นเดือนพฤษภาคม ค.ศ. 1962 ในปีนั้น ก็เปิดรับนักเรียนระดับชั้นประถมศึกษาปีที่ 5 และปีต่อมา ก็ได้เปิดชั้นประถมศึกษาปีที่ 6 ไล่ขึ้นมาจนถึงชั้นมัธยมศึกษาปีที่ 3</p>
      <p>ใน ค.ศ. 1978 จึงได้ขยายชั้นเรียนเป็นตั้งแต่ระดับประถมศึกษาปีที่ 1 จนถึงมัธยมศึกษาปีที่ 6 นักเรียนสำเร็จการศึกษาระดับชั้นมัธยมศึกษาปีที่ 6 รุ่นแรกใน ค.ศ. 1983 และเมื่อเกิดวิกฤตเศรษฐกิจขึ้นใน ค.ศ. 1987 คณะกรรมการโรงเรียนจึงปิดระดับชั้นมัธยมศึกษาตอนปลายชั่วคราว ปัจจุบันโรงเรียนได้เปิดทำการสอนระดับมัธยมศึกษาตอนปลาย และมีนักเรียนที่สำเร็จการศึกษาในระดับมัธยมศึกษาปีที่ 6 สอบเข้ามหาวิทยาลัยชั้นนำของประเทศได้เป็นจำนวนมาก</p>
    </section>
  </main>
</div>

<style>
  .page {
    overflow: hidden;
  }
  header {
    padding-top: var(--navheight);
    min-height: 66vh;
    font-size: 1.1rem;
    position: relative;
  }
  header::after {
    content: '';
    position: absolute;
    inset: 0;
    width: 100%;
    height: 100%;
    z-index: -1;
    background: url(/src/images/vision/bg_vision.jpg) no-repeat center center;
    background-size: cover;
    opacity: 0.15;
  }
  header h1 {
    font-size: 2rem;
    font-weight: 600;
    padding-top: 1rem;
  }
  p {
    max-width: 960px;
    margin: auto;
    margin-bottom: 2rem;
  }
</style>