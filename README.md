<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Laid by Ivy | Booking</title>
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display&family=Montserrat&display=swap" rel="stylesheet">
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: 'Montserrat', sans-serif;
      background: #0e0e0e;
      color: #fff;
      line-height: 1.6;
      padding: 20px;
    }

    header {
      text-align: center;
      margin-bottom: 40px;
    }

    header h1 {
      font-family: 'Playfair Display', serif;
      font-size: 3em;
      color: #fff;
      letter-spacing: 1px;
    }

    header p {
      color: #ffcba4;
      font-size: 1.1em;
      margin-top: 10px;
    }

    .calendar-visual {
      background: #1a1a1a;
      padding: 20px;
      border-radius: 10px;
      margin: 40px auto;
      max-width: 600px;
      text-align: center;
    }

    .calendar-visual h2 {
      font-family: 'Playfair Display', serif;
      font-size: 2em;
      margin-bottom: 20px;
      color: #ffb88c;
    }

    .calendar-grid {
      display: grid;
      grid-template-columns: repeat(7, 1fr);
      gap: 10px;
      font-size: 0.9em;
    }

    .calendar-grid div {
      padding: 10px;
      border: 1px solid #444;
      border-radius: 5px;
      background: #2a2a2a;
    }

    .book-btn {
      display: inline-block;
      margin: 40px auto;
      padding: 16px 32px;
      font-size: 1.2em;
      font-weight: bold;
      color: #fff;
      background: #ff8c42;
      text-decoration: none;
      border-radius: 50px;
      box-shadow: 0 0 15px #ff8c42;
      transition: all 0.3s ease;
    }

    .book-btn:hover {
      background: #ffcba4;
      color: #000;
      box-shadow: 0 0 25px #ffcba4;
    }

    footer {
      margin-top: 60px;
      text-align: center;
      font-size: 0.9em;
      color: #888;
    }

    @media (max-width: 600px) {
      .calendar-grid {
        grid-template-columns: repeat(4, 1fr);
      }
    }
  </style>
</head>
<body>

  <header>
    <h1>Laid by Ivy</h1>
    <p>Professional Wig Installation & Sew-ins</p>
  </header>

  <section class="calendar-visual">
    <h2>Available Booking Days</h2>
    <div class="calendar-grid">
      <div>Sun</div><div>Mon</div><div>Tue</div><div>Wed</div>
      <div>Thu</div><div>Fri</div><div>Sat</div>
      <div>✔️</div><div>✔️</div><div>✔️</div><div>✔️</div>
      <div>✔️</div><div>✔️</div><div>✔️</div>
    </div>
    <p style="margin-top: 20px; font-size: 0.95em; color: #ccc;">
      Bookings are available daily from 9AM - 11PM
    </p>
  </section>

  <div style="text-align:center;">
    <a class="book-btn" href="https://laidbyivyco.as.me/schedule/6188404f?fbclid=PAdGRleAMonDRleHRuA2FlbQIxMAABpyN6sm79a_Qkjcj4Rn1MbCf9J7e0el9Ps4j3oQcpVWrpsZo2zHB2vLiBt_F7_aem_dw_Oj_I3RlTTT0DaF5NfmQ" target="_blank">
      📅 BOOK NOW
    </a>
  </div>

  <footer>
    &copy; 2025 Laid by Ivy · <a style="color:#ffb88c;" href="mailto:yvaellacedar@gmail.com">Contact Us</a>
  </footer>

</body>
</html>
