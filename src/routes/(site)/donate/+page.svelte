<svelte:head>
	<title>Donate</title>
</svelte:head>

<div class="page">
  <header class="flex flex-col justify-start items-center text-center">
    <img src="/src/public/SCAlogo2023.png" alt="SCA logo" draggable="false" class="select-none">
    <span class="text-2xl">โรงเรียนสามมุกคริสเตียนวิทยา</span>
    <span>ขอเชิญชวนทุกท่าน</span>
    <div class="absolute top-1/2">
      <h1>ร่วมบริจาคเพื่อการศึกษา</h1>
      <span>ผ่านทางระบบบริจาคอิเล็กทรอนิกส์ (e-Donation)</span>
    </div>
  </header>
  <main>
    <!-- <section>
      <h2>บริจาคผ่านการโอนเข้าบัญชีธนาคารกรุงไทย</h2>
      <div class="cards py-4">
        <div class="card">
          โอนเข้าบัญชีธนาคารกรุงไทย <br>ชื่อบัญชี:โรงเรียนสามมุกคริสเตียนวิทยา<br>เลขบัญชี:464-6-00066-0
        </div>
        <div class="card">
          ส่งหลักฐานการโอนเงินเพื่อขอรับใบเสร็จได้ทาง <br>Line ID: scadonation<br>พร้อมแนบ
        </div>
        <div class="card">
          1.รูปบัตรประชาชน
          2.E-mail
          3.เบอร์โทรศัพท์
        </div>
      </div>
    </section> -->
    <section>
      <h2>บริจาคผ่านการสแกน QR Code PromtPay</h2>
      <div class="slider py-4">
        <div class="cards">
          <div class="card">
            QR
          </div>
          <div class="card">
            เปิดใช้งาน App Mobile Banking ของท่าน
          </div>
          <div class="card">
            เลือกเมนูสแกน และ สแกน QR Code
          </div>
          <div class="card">
            เมื่อพบข้อความ ให้ธนาคารที่เกี่ยวข้องเปิดเผยข้อมูลรายการนี้ให้แก่กรมสรรพากร และ/หรือหน่วยรับบริจาคเพื่อการใช้สิทธิลดหย่อนภาษี
          </div>
          <div class="card">
            ตรวจสอบชื่อบัญชี: โรงเรียนสามมุกคริสเตียนวิทยา หรือ เป๋าตุง เติมบุญ
            เลขผู้เสียภาษี: 0994000150822
          </div>
          <div class="card">
            ระบุลงในบันทึกว่า "บริจาคเพื่อการศึกษา" ระบุจำนวนเงินและกดยืนยัน
          </div>
        </div>
        <div class="control">
          <input type="radio" name="cards" id="card1" checked>
          <input type="radio" name="cards" id="card2">
          <input type="radio" name="cards" id="card3">
          <input type="radio" name="cards" id="card4">
          <input type="radio" name="cards" id="card5">
          <input type="radio" name="cards" id="card6">
        </div>
      </div>
    </section>
  </main>
</div>

<style>
  .page {
    padding-top: var(--navheight);
    overflow: hidden;
  }
  .page::after {
    content: '';
    position: absolute;
    inset: 0;
    width: 100%;
    height: 100%;
    z-index: -1;
    background: url(/src/images/bg_donate.jpg) no-repeat center top;
    background-size: cover;
    opacity: 0.15;
  }
  header {
    min-height: calc(100vh - var(--navheight));
    font-size: 1.1rem;
  }
  header img {
    padding: 1.5rem;
		width: clamp(7.5rem, 15%, 10rem);
	}
  header h1 {
    font-size: 2rem;
    font-weight: 600;
    padding-top: 1rem;
  }

  main {
    padding: 2.5rem 0;
    text-align: center;
  }
  h2 {
    font-size: 1.25rem;
    font-weight: 600;
  }
  .slider {
    display: block;
    padding: 5%;
  }
  .cards {
    display: flex;
    justify-content: center;
  }
  .card {
    display: none;
    flex-wrap: wrap;
    align-content: space-around;
    justify-content: center;
    width: 300px;
    height: 480px;
    border: 3px solid black;
    border-radius: 15px;
  }
  .slider:has(#card1:checked) .cards .card:nth-child(1) {
    display: flex;
  }
  .slider:has(#card2:checked) .cards .card:nth-child(2) {
    display: flex;
  }
  .slider:has(#card3:checked) .cards .card:nth-child(3) {
    display: flex;
  }
  .slider:has(#card4:checked) .cards .card:nth-child(4) {
    display: flex;
  }
  .slider:has(#card5:checked) .cards .card:nth-child(5) {
    display: flex;
  }
  .slider:has(#card6:checked) .cards .card:nth-child(6) {
    display: flex;
  }
</style>