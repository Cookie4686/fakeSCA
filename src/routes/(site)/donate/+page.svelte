<script>
	import Slider from "../../../components/slider.svelte";

  const cards1 = [
    {id:1,zoom:false,src:'/src/images/donate/logo-krungthai.png',alt:'Krungthai logo',text:'โอนเข้าบัญชีธนาคารกรุงไทย<br/>ชื่อบัญชี: โรงเรียนสามมุกคริสเตียนวิทยา<br/>เลขบัญชี: 464-6-00066-0'},
    {id:2,zoom:true,src:'/src/images/donate/line-qr.png',alt:'Line QR',text:'ส่งหลักฐานการโอนเงินเพื่อขอรับใบเสร็จได้ทาง Line ID: scadonation พร้อมแนบ<br/>1.รูปบัตรประชาชน<br/>2.E-mail<br/>3.เบอร์โทรศัพท์'},
    {id:3,zoom:false,src:'',alt:'',text:'หากส่งหลักฐานภายในวันที่โอน จะได้รับใบรับเงินบริจาคในวันรุ่งขึ้น'},
    {id:4,zoom:false,src:'',alt:'',text:'หากไม่ได้รับใบรับเงินบริจาคภายใน 3 วันทำการหลังโอนเงิน สามารถสอบถามเข้ามาได้ทางไลน์ หรืออีเมล officer@sca.ac.th'},
    {id:5,zoom:false,src:'/src/images/donate/logo-rd.png',alt:'Revenue Department logo',text:"ผู้บริจาคสามารถเข้าตรวจสอบด้วยตนเองได้ที่เว็บไซต์ของกรมสรรพากร <a href='https://epayapp.rd.go.th/rd-edonation/portal/for-donor' target='_blank'>https://epayapp.rd.go.th/rd-edonation/portal/for-donor</a>"},
  ]
  const cards2 = [
    {id:1,zoom:false,src:'/src/images/donate/mobile-banking.png',alt:'',text:'เปิดใช้งาน App Mobile Banking ของท่าน'},
    {id:2,zoom:true,src:'/src/images/donate/promtpay-qr.png',alt:'',text:'เลือกเมนูสแกน และ สแกน QR Code<br/>(กดที่รูปเพื่อ zoom)'},
    {id:3,zoom:false,src:'',alt:'',text:'เมื่อพบข้อความ<br/>ให้ธนาคารที่เกี่ยวข้องเปิดเผยข้อมูลรายการนี้ให้แก่กรมสรรพากร และ/หรือหน่วยรับบริจาคเพื่อการใช้สิทธิลดหย่อนภาษี<br/>ให้กดเลือกยอมรับ'},
    {id:4,zoom:false,src:'',alt:'',text:'ตรวจสอบ<br/>ชื่อบัญชี: โรงเรียนสามมุกคริสเตียนวิทยา<br/>หรือ<br/>เป๋าตุง เติมบุญ<br/>เลขผู้เสียภาษี: 0994000150822'},
    {id:5,zoom:false,src:'',alt:'',text:'ระบุลงในบันทึกว่า "บริจาคเพื่อการศึกษา"<br/>ระบุจำนวนเงินและกดยืนยัน'},
    ]
</script>

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
    <section>
      <h2>บริจาคผ่านการโอนเข้าบัญชีธนาคารกรุงไทย</h2>
      <Slider num='1' cards={cards1}></Slider>
    </section>
    <section>
      <h2>บริจาคผ่านการสแกน QR Code PromtPay</h2>
      <Slider num='2' cards={cards2}></Slider>
    </section>
    <section>
      <h2 class="thank">Thank You!</h2>
      <p class="thank-text">ขอบคุณทุกท่านที่ให้การสนับสนุนพันธกิจของโรงเรียนสามมุกคริสเตียนวิทยา<br/>เงินบริจาคของท่านจะถูกนำไปใช้เพื่อพัฒนาโรงเรียนโดยคำนึงถึงประโยชน์ของนักเรียนและผู้ปกครองเป็นหลัก</p>
      <div class="flex justify-center">
        <p style="max-width: 500px;">หมายเหตุ:<br/>ผู้ที่บริจาคสนับสนุนการศึกษา เพื่อใช้สิทธิ์ลดหย่อนภาษี 2 เท่า<br/>จะต้องบริจาคผ่าน ระบบบริจาคอิเล็กทรอนิกส์ (2 ช่องทางข้างต้น) เท่านั้น<br/>และลดหย่อนได้ตามที่จ่ายจริง แต่ไม่เกิน 10% ของรายได้หลังหักค่าใช้จ่าย และค่าลดหย่อนอื่นๆที่ไม่ใช่เงินบริจาค</p>
      </div>
    </section>
  </main>
</div>

<style>
  .page {
    overflow: hidden;
  }
  header {
    padding-top: var(--navheight);
    min-height: 100vh;
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
    background: url(/src/images/donate/bg_donate.jpg) no-repeat center top;
    background-size: cover;
    opacity: 0.15;
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

  .thank {
    font-size: 2rem;
    margin-bottom: 0.5rem;
  }
  .thank-text {
    font-size: 1.25rem;
    margin-bottom: 2.5rem;
  }
</style>