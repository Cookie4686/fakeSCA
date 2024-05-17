<svelte:head>
  <title>Our Vision</title>
</svelte:head>

<div class="page">
  <header class="flex flex-col justify-start items-center text-center">
    <div class="absolute top-1/2">
      <h1>วิสัยทัศน์และพันธกิจ</h1>
    </div>
  </header>
  <main>
    <section>
      <h2>ปรัชญาของโรงเรียน</h2>
      <p>"มุ่งเสริมเยาวชนด้วยการศึกษาที่มีคุณภาพ ให้เป็นพลเมืองดีของชาติบ้านเมืองในอุดมคติแบบคริสเตียน"</p>
    </section>
    <section>
      <h2>วิสัยทัศน์ของโรงเรียน</h2>
      <p>"โรงเรียนประจำชั้นเลิศ ก่อเกิดภาวะผู้นำ ก้าวล้ำสู่ Happiness School"</p>
    </section>
    <section>
      <h2>พันธกิจของโรงเรียน</h2>
      <p>โรงเรียนสามมุกคริสเตียนวิทยามุ่งพัฒนาให้นักเรียนเป็นผู้ที่มีคุณธรรม จริยธรรม มีระเบียบวินัย มีความรู้ด้านวิชาการก้าวทันเทคโนโลยี มีสุนทรียศาสตร์ มีสุขภาพแข็งแรง รักษ์สิ่งแวดล้อม สืบสานความเป็นไทย ช่วยเหลือสังคมและอยู่ร่วมกับผู้อื่นได้อย่างมีความสุขในอุดมคติแบบคริสเตียน</p>
    </section>
    <section>
      <h2>คติพจน์ของโรงเรียน</h2>
      <p>"ศึกษาดีมีวินัย ใจสัตย์ซื่อ ถือคุณธรรม"</p>
    </section>
    <section>
      <h2>อัตลักษณ์ของโรงเรียน</h2>
      <p>"ลูกสามมุกคริสเตียน เป็นพลเมืองดี มีวินัย ใส่ใจคุณธรรม"</p>
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
  }
</style>