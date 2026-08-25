# gocdaonuong
Website Góc Đảo Nướng
<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>Góc Đảo Nướng</title>
  <meta
    name="description"
    content="Góc Đảo Nướng - 56 Nguyễn Thông, Xóm Cội. Hải sản nướng, món ngon và đặt bàn nhanh."
  >

  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link
    href="https://fonts.googleapis.com/css2?family=Be+Vietnam+Pro:wght@400;500;600;700;800&display=swap"
    rel="stylesheet"
  >

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      font-family: "Be Vietnam Pro", Arial, sans-serif;
      background:
        radial-gradient(
          circle at top,
          rgba(255, 145, 0, 0.18),
          transparent 360px
        ),
        #050505;
      color: #ffffff;
      min-height: 100vh;
    }

    a {
      text-decoration: none;
      color: inherit;
    }

    .container {
      width: min(92%, 760px);
      margin: 0 auto;
      padding: 34px 0 60px;
    }

    /* =========================
       LOGO
    ========================== */

    .logo-wrapper {
      display: flex;
      justify-content: center;
      margin-top: 6px;
      margin-bottom: 25px;
    }

    .logo-circle {
      width: 150px;
      height: 150px;
      border-radius: 50%;
      overflow: hidden;
      border: 5px solid #ff9800;
      background: #111111;

      display: flex;
      align-items: center;
      justify-content: center;

      box-shadow:
        0 0 15px rgba(255, 152, 0, 0.85),
        0 0 35px rgba(255, 152, 0, 0.4);
    }

    .logo-circle img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      display: block;
    }

    .logo-fallback {
      display: none;
      width: 100%;
      height: 100%;
      align-items: center;
      justify-content: center;
      text-align: center;
      font-weight: 800;
      font-size: 22px;
      color: #ffab18;
      padding: 14px;
    }

    /* =========================
       HERO
    ========================== */

    .hero {
      text-align: center;
      margin-bottom: 28px;
    }

    .hero h1 {
      color: #ffa914;
      font-size: clamp(38px, 10vw, 65px);
      line-height: 1.1;
      font-weight: 800;

      text-shadow:
        0 0 9px rgba(255, 165, 0, 0.3),
        0 0 25px rgba(255, 145, 0, 0.22);

      margin-bottom: 22px;
    }

    .address {
      font-size: clamp(18px, 5vw, 28px);
      line-height: 1.5;
      color: #eeeeee;
    }

    .address span {
      margin-right: 7px;
    }

    /* =========================
       BUTTONS
    ========================== */

    .actions {
      display: flex;
      flex-direction: column;
      gap: 18px;
      margin-top: 35px;
    }

    .action-btn {
      min-height: 92px;
      width: 100%;
      border-radius: 25px;

      display: flex;
      justify-content: center;
      align-items: center;

      padding: 18px 22px;

      font-size: clamp(18px, 5vw, 29px);
      font-weight: 800;
      text-align: center;

      transition:
        transform 0.2s ease,
        filter 0.2s ease;

      box-shadow: 0 10px 30px rgba(0,0,0,0.25);
    }

    .action-btn:active {
      transform: scale(0.98);
    }

    .action-btn:hover {
      filter: brightness(1.08);
    }

    .phone-btn {
      background: linear-gradient(
        100deg,
        #ff9400,
        #ff5700
      );
    }

    .zalo-btn {
      background: linear-gradient(
        100deg,
        #0868ff,
        #1137bf
      );
    }

    .facebook-btn {
      background: linear-gradient(
        100deg,
        #1557e8,
        #43369c
      );
    }

    .btn-icon {
      margin-right: 12px;
      font-size: 1.15em;
    }

    /* =========================
       SECTION
    ========================== */

    .section {
      margin-top: 70px;
      background: rgba(15, 15, 15, 0.94);
      border: 1px solid rgba(255, 153, 0, 0.35);
      border-radius: 35px;
      padding: 38px 28px;

      box-shadow:
        0 14px 50px rgba(0,0,0,0.35),
        inset 0 0 25px rgba(255, 145, 0, 0.025);
    }

    .section-title {
      text-align: center;
      font-size: clamp(29px, 8vw, 47px);
      font-weight: 800;
      color: #ffae1a;
      margin-bottom: 30px;
    }

    /* =========================
       MENU
    ========================== */

    .menu-list {
      width: 100%;
    }

    .menu-item {
      display: grid;
      grid-template-columns: 1fr auto;
      align-items: center;
      gap: 15px;

      padding: 25px 0;
      border-bottom: 1px solid #262626;
    }

    .menu-item:last-child {
      border-bottom: none;
    }

    .menu-name {
      color: #f4f4f4;
      font-size: clamp(18px, 4.8vw, 27px);
      line-height: 1.4;
    }

    .menu-price {
      color: #ffae18;
      font-weight: 800;
      font-size: clamp(18px, 4.8vw, 27px);
      white-space: nowrap;
    }

    /* =========================
       INFORMATION
    ========================== */

    .info-box {
      text-align: center;
      line-height: 1.8;
      font-size: 18px;
      color: #dddddd;
    }

    .info-box strong {
      color: #ffad18;
    }

    .footer {
      text-align: center;
      margin-top: 45px;
      padding: 25px 10px;
      color: #858585;
      font-size: 14px;
      line-height: 1.7;
    }

    /* =========================
       MOBILE
    ========================== */

    @media (max-width: 520px) {
      .container {
        width: 90%;
        padding-top: 27px;
      }

      .logo-circle {
        width: 125px;
        height: 125px;
      }

      .hero h1 {
        margin-top: 5px;
      }

      .action-btn {
        min-height: 80px;
        border-radius: 21px;
        padding: 15px;
      }

      .section {
        margin-top: 58px;
        padding: 30px 22px;
        border-radius: 28px;
      }

      .menu-item {
        padding: 22px 0;
      }
    }
  </style>
</head>

<body>

  <main class="container">

    <!-- =========================
         LOGO
         File ảnh cần tên: logo.jpg
    ========================== -->

    <div class="logo-wrapper">
      <div class="logo-circle">

        <img
          src="logo.jpg"
          alt="Logo Góc Đảo Nướng"
          onerror="
            this.style.display='none';
            document.getElementById('logoFallback').style.display='flex';
          "
        >

        <div
          class="logo-fallback"
          id="logoFallback"
        >
          🔥<br>GÓC ĐẢO<br>NƯỚNG
        </div>

      </div>
    </div>


    <!-- =========================
         TÊN QUÁN
    ========================== -->

    <section class="hero">

      <h1>Góc Đảo Nướng</h1>

      <div class="address">
        <span>📍</span>
        56 Nguyễn Thông • Xóm Cội
      </div>

    </section>


    <!-- =========================
         NÚT LIÊN HỆ
    ========================== -->

    <section class="actions">

      <!-- GỌI ĐIỆN -->
      <a
        class="action-btn phone-btn"
        href="tel:0915879803"
      >
        <span class="btn-icon">📞</span>
        GỌI NGAY: 0915 879 803
      </a>


      <!-- ZALO -->
      <a
        class="action-btn zalo-btn"
        href="https://zalo.me/0915879803"
        target="_blank"
        rel="noopener noreferrer"
      >
        <span class="btn-icon">💙</span>
        ĐẶT BÀN QUA ZALO
      </a>


      <!-- FACEBOOK -->
      <!--
        Sau này bạn gửi link Facebook,
        tôi sẽ thay link bên dưới cho bạn.
      -->

      <a
        class="action-btn facebook-btn"
        href="#"
        onclick="
          alert('Bạn hãy thêm đường dẫn Facebook của Góc Đảo Nướng vào mã.');
          return false;
        "
      >
        <span class="btn-icon">💬</span>
        ĐẶT BÀN QUA FACEBOOK
      </a>

    </section>


    <!-- =========================
         MENU
    ========================== -->

    <section class="section">

      <h2 class="section-title">
        🔥 Menu nổi bật
      </h2>

      <div class="menu-list">


        <div class="menu-item">
          <div class="menu-name">
            Hàu nướng phô mai
          </div>

          <div class="menu-price">
            7.000đ
          </div>
        </div>


        <div class="menu-item">
          <div class="menu-name">
            Hàu nướng mỡ hành
          </div>

          <div class="menu-price">
            6.000đ
          </div>
        </div>


        <div class="menu-item">
          <div class="menu-name">
            Hàu hấp sả
          </div>

          <div class="menu-price">
            50.000đ/kg
          </div>
        </div>


        <div class="menu-item">
          <div class="menu-name">
            Cháo hàu
          </div>

          <div class="menu-price">
            25.000đ
          </div>
        </div>


        <div class="menu-item">
          <div class="menu-name">
            Sò nướng mỡ hành
          </div>

          <div class="menu-price">
            Liên hệ
          </div>
        </div>


        <div class="menu-item">
          <div class="menu-name">
            Hải sản nướng
          </div>

          <div class="menu-price">
            Liên hệ
          </div>
        </div>


      </div>

    </section>


    <!-- =========================
         THÔNG TIN
    ========================== -->

    <section class="section">

      <h2 class="section-title">
        📍 Góc Đảo Nướng
      </h2>

      <div class="info-box">

        <p>
          <strong>Địa chỉ:</strong><br>
          56 Nguyễn Thông • Xóm Cội
        </p>

        <br>

        <p>
          <strong>Điện thoại:</strong><br>
          0915 879 803
        </p>

        <br>

        <p>
          🍺 Bia + Nước ngọt các loại
        </p>

      </div>

    </section>


    <!-- =========================
         FOOTER
    ========================== -->

    <footer class="footer">

      © 2026 Góc Đảo Nướng<br>
      56 Nguyễn Thông • Xóm Cội

    </footer>

  </main>

</body>
</html>
