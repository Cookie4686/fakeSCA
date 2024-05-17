<svelte:head>
  <title>General Information</title>
</svelte:head>

<div class="page">
  <header class="flex flex-col justify-start items-center text-center">
    <div class="absolute top-1/2">
      <h1>ข้อมูลทั่วไป</h1>
    </div>
  </header>
  <main>
    <section>
      <h2>ข้อมูลเกี่ยวกับโรงเรียน</h2>
      <p>โรงเรียนสามมุกคริสเตียนวิทยา เป็นโรงเรียนประจำ แบบสหศึกษา คือมีทั้งนักเรียนชายและนักเรียนหญิง อยู่ประจำที่โรงเรียน โดยแบ่งหอพักนักเรียนชายและนักเรียนหญิง มีอาจารย์ดูแลอยู่ประจำหอพักที่โรงเรียนอยู่ที่ 166 ถนนบางแสน-อ่างศิลา ตำบลแสนสุข อำเภอเมืองชลบุรี จังหวัดชลบุรี สังกัดสำนักงานเขตพื้นที่การศึกษาชลบุรี เขต 1</p>
      <p>เปิดสอนตั้งแต่ระดับชั้นประถมศึกษาปีที่ 4 จนถึงระดับชั้นมัธยมศึกษาปีที่ 6 มีเนื้อที่ประมาณ 50 ไร่ เปิดสอนตามหลักสูตรการศึกษาขั้นพื้นฐาน พุทธศักราช 2544 ระดับชั้นประถมศึกษา มัธยมศึกษาตอนต้น และมัธยมศึกษาตอนปลาย โดยสอนวิชาภาษาอังกฤษ และภาษาจีนในทุกระดับชั้น วัตถุประสงค์ในการจัดตั้งเพื่อให้การศึกษาแก่เยาวชนตามหลักคริสตธรรม โดยไม่หวังกำไรในเชิงธุรกิจ นักเรียนชั้นประถมศึกษาปีที่ 1-3 เป็นนักเรียนไป-กลับ และชั้นประถมศึกษาปีที่ 4- มัธยมศึกษาปีที่ 6 เป็นนักเรียนประจำ</p>
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
    background: url(/src/lib/assets/vision/bg_vision.jpg) no-repeat center center;
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