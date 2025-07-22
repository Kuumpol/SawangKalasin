<!DOCTYPE html>
<html lang="th">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>ศูนย์กู้ภัยสว่างกาฬสินธุ์</title>
  <style>
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      margin: 0;
      padding: 0;
      background-color: #f9f9f9;
      color: #333;
    }

    header {
      background-color: #3900f6;
      color: white;
      padding: 30px 20px;
      text-align: center;
    }

    nav {
      background-color: #ff0000;
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      padding: 10px 0;
      box-shadow: 0 2px 5px rgba(0,0,0,0.2);
    }

    nav a {
      color: white;
      text-decoration: none;
      margin: 10px 20px;
      font-weight: bold;
      padding: 8px 16px;
      border-radius: 20px;
      transition: background 0.3s;
    }

    nav a:hover {
      background-color: rgba(255,255,255,0.2);
    }

    main {
      padding: 40px 20px;
      max-width: 1000px;
      margin: auto;
    }

    section {
      background: white;
      margin-bottom: 40px;
      padding: 30px;
      border-radius: 12px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.08);
      display: none;
    }

    section.active {
      display: block;
    }

    h2 {
      color: #c62828;
    }

    footer {
      text-align: center;
      padding: 20px;
      background-color: #c62828;
      color: white;
      margin-top: 50px;
    }

    .donation-form {
      margin-top: 20px;
    }

    .donation-form input[type="file"] {
      padding: 10px;
    }

    .donation-form button {
      margin-top: 10px;
      padding: 10px 20px;
      background-color: #4caf50;
      color: white;
      border: none;
      border-radius: 6px;
      cursor: pointer;
    }

    .donation-form button:hover {
      background-color: #388e3c;
    }

    .home {
      text-align: center;
    }

    @media (max-width: 600px) {
      nav {
        flex-direction: column;
        align-items: center;
      }

      nav a {
        margin: 5px 0;
      }
    }
  </style>
</head>
<body>

  <header>
    <h1>ศูนย์กู้ภัยสว่างกาฬสินธุ์</h1>
    <p>เราพร้อมช่วยเหลือ 24 ชั่วโมง ทุกชีวิตมีค่า</p>
  </header>

  <nav>
    <a onclick="showSection('home')">หน้าแรก</a>
    <a onclick="showSection('mission')">ภารกิจ</a>
    <a onclick="showSection('departments')">ฝ่ายต่างๆ</a>
    <a onclick="showSection('donation')">บริจาค</a>
    <a onclick="showSection('contact')">ติดต่อ</a>
  </nav>

  <main>
    <div id="home" class="home active">
      <h2>ยินดีต้อนรับสู่ศูนย์กู้ภัยสว่างกาฬสินธุ์</h2>
      <p>เราคือองค์กรจิตอาสาที่มุ่งมั่นในการช่วยเหลือชีวิตผู้ประสบภัยในทุกสถานการณ์</p>
    </div>

    <section id="mission">
      <h2>ภารกิจหลักของเรา</h2>
      <ul>
        <li>ช่วยเหลือผู้ประสบอุบัติเหตุบนถนน</li>
        <li>กู้ภัยน้ำท่วมและภัยพิบัติธรรมชาติ</li>
        <li>ขนส่งผู้ป่วยฉุกเฉิน</li>
        <li>ดับเพลิงเบื้องต้น</li>
        <li>ฝึกอบรมจิตอาสา</li>
      </ul>
    </section>

    <section id="departments">
      <h2>ฝ่ายปฏิบัติงานภายในศูนย์</h2>
      <ul>
        <li>ฝ่ายปฏิบัติการภาคสนาม</li>
        <li>ฝ่ายสนับสนุนการแพทย์</li>
        <li>ฝ่ายสื่อสารและควบคุม</li>
        <li>ฝ่ายพัฒนาและฝึกอบรม</li>
        <li>ฝ่ายบริหารและการเงิน</li>
      </ul>
    </section>

    <section id="donation">
      <h2>ร่วมบริจาคเพื่อสนับสนุนภารกิจกู้ภัย</h2>
      <p><strong>บัญชี:</strong><br>ธนาคารกรุงเทพ<br>มูลนิธิสว่างกาฬสินธุ์<br>เลขที่: 315-4-34390-3</p>
      <p>📞 ติดต่อ: 080-228-1685 | Facebook: <a href="#">สว่างกาฬสินธุ์</a></p>
      <p>สามารถแนบสลิปการโอนเพื่อเก็บบันทึกได้ด้านล่าง</p>

      <form class="donation-form" id="donationForm">
        <input type="file" id="slipFile" required />
        <button type="submit">📤 ส่งสลิป</button>
      </form>

      <p id="uploadStatus"></p>
    </section>

    <section id="contact">
      <h2>ข้อมูลติดต่อ</h2>
      <p>📞 โทร: 043-840-243 | สายด่วน: 1669</p>
      <p>📧 อีเมล: sawangkalasin5757e@gmail.com</p>
      <p>📍 ที่อยู่: 456 ถ.ดงปอ อ.เมือง จ.กาฬสินธุ์ 46000</p>
    </section>
  </main>

  <footer>
    &copy; 2025 ศูนย์กู้ภัยสว่างกาฬสินธุ์ | ร่วมด้วยช่วยกันเพื่อชีวิต
  </footer>

  <script>
    function showSection(id) {
      const sections = document.querySelectorAll('section, .home');
      sections.forEach(sec => sec.classList.remove('active'));
      document.getElementById(id).classList.add('active');
      window.scrollTo({ top: 0, behavior: 'smooth' });
    }

    const form = document.getElementById("donationForm");
    form.addEventListener("submit", async function (e) {
      e.preventDefault();
      const file = document.getElementById("slipFile").files[0];
      const formData = new FormData();
      formData.append("file", file);

      const response = await fetch("https://drive.google.com/drive/folders/1eENRUOdetuXjjhviWqhoR41GjsDW1C9W?usp=sharing", {
        method: "POST",
        body: formData
      });

      const result = await response.text();
      document.getElementById("uploadStatus").innerText = result;
    });
  </script>
</body>
</html>
