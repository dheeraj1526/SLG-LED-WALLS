<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>SLG LED WALLS | Professional LED Solutions</title>
  <style>
    /* Reset & base */
    * {
      margin: 0; padding: 0; box-sizing: border-box;
    }
    body {
      font-family: 'Poppins', sans-serif;
      background: linear-gradient(135deg, #0a0a0a 0%, #121212 100%);
      color: #fff;
      overflow-x: hidden;
      scroll-behavior: smooth;
    }
    a {
      color: inherit;
      text-decoration: none;
    }

    /* Container */
    .container {
      max-width: 1200px;
      margin: 0 auto;
      padding: 0 30px;
    }

    /* Header */
    header {
      padding: 30px 0;
      text-align: center;
      position: relative;
      z-index: 10;
      animation: fadeDown 1s ease forwards;
      opacity: 0;
    }
    header h1 {
      font-size: 3rem;
      letter-spacing: 0.1em;
      color: #00ff99;
      text-shadow: 0 0 15px #00ff99;
      animation: glowText 2s ease-in-out infinite alternate;
    }
    header p {
      margin-top: 10px;
      font-size: 1.2rem;
      color: #a1f5b6;
      font-weight: 600;
    }

    /* Hero Section */
    .hero {
      display: flex;
      align-items: center;
      justify-content: space-between;
      margin-top: 60px;
      animation: fadeUp 1s ease forwards;
      opacity: 0;
    }
    .hero-text {
      flex: 1;
      padding-right: 40px;
    }
    .hero-text h2 {
      font-size: 2.5rem;
      margin-bottom: 20px;
      font-weight: 700;
      color: #00ffa8;
    }
    .hero-text p {
      font-size: 1.15rem;
      line-height: 1.6;
      color: #ddd;
      margin-bottom: 40px;
    }
    .hero-text button {
      background: #00ff99;
      border: none;
      padding: 15px 40px;
      font-size: 1.1rem;
      font-weight: 700;
      border-radius: 50px;
      cursor: pointer;
      box-shadow: 0 0 20px #00ff99;
      transition: background 0.3s ease, box-shadow 0.3s ease;
    }
    .hero-text button:hover {
      background: #00cc7a;
      box-shadow: 0 0 30px #00cc7a;
    }

    /* Hero Image */
    .hero-image {
      flex: 1;
      perspective: 1200px;
    }
    .hero-image img {
      width: 100%;
      max-width: 480px;
      border-radius: 25px;
      box-shadow: 0 0 50px #00ff99;
      transform-style: preserve-3d;
      animation: float 4s ease-in-out infinite;
    }

    /* Features Section */
    .features {
      margin: 80px 0;
      text-align: center;
      animation: fadeUp 1s ease forwards;
      opacity: 0;
    }
    .features h3 {
      font-size: 2rem;
      margin-bottom: 40px;
      color: #00ff99;
      text-shadow: 0 0 10px #00ff99;
    }
    .feature-list {
      display: flex;
      justify-content: space-around;
      flex-wrap: wrap;
      gap: 40px;
    }
    .feature {
      background: #111;
      padding: 30px;
      border-radius: 20px;
      flex: 1 1 250px;
      box-shadow: 0 0 25px #00ff99aa;
      transition: transform 0.3s ease;
      cursor: default;
    }
    .feature:hover {
      transform: translateY(-10px);
      box-shadow: 0 0 40px #00ff99ee;
    }
    .feature h4 {
      font-size: 1.5rem;
      margin-bottom: 15px;
      color: #00ffcc;
    }
    .feature p {
      color: #bbb;
      line-height: 1.4;
      font-size: 1rem;
    }

    /* Contact Section */
    .contact {
      background: linear-gradient(90deg, #003300 0%, #006633 100%);
      padding: 50px 30px;
      border-radius: 30px;
      text-align: center;
      box-shadow: 0 0 50px #00ff99aa;
      animation: fadeUp 1s ease forwards;
      opacity: 0;
    }
    .contact h3 {
      font-size: 2rem;
      margin-bottom: 15px;
      color: #00ff99;
      text-shadow: 0 0 12px #00ff99;
    }
    .contact p {
      font-size: 1.3rem;
      margin-bottom: 30px;
      color: #cfffcf;
    }
    .contact a {
      display: inline-block;
      background: #00ff99;
      color: #000;
      padding: 18px 45px;
      font-size: 1.3rem;
      font-weight: 700;
      border-radius: 50px;
      box-shadow: 0 0 40px #00ff99;
      transition: background 0.3s ease, box-shadow 0.3s ease;
    }
    .contact a:hover {
      background: #00cc7a;
      box-shadow: 0 0 50px #00cc7a;
    }

    /* Fixed Contact Button */
    .contact-fixed {
      position: fixed;
      bottom: 30px;
      right: 30px;
      background: #00ff99;
      border-radius: 50%;
      width: 70px;
      height: 70px;
      box-shadow: 0 0 30px #00ff99;
      display: flex;
      justify-content: center;
      align-items: center;
      cursor: pointer;
      animation: pulseContact 2s infinite alternate;
      z-index: 100;
      transition: background 0.3s ease;
    }
    .contact-fixed:hover {
      background: #00cc7a;
      box-shadow: 0 0 45px #00cc7a;
    }
    .contact-fixed svg {
      width: 36px;
      height: 36px;
      fill: #000;
    }

    /* Animations */
    @keyframes fadeDown {
      to {
        opacity: 1;
        transform: translateY(0);
      }
      from {
        opacity: 0;
        transform: translateY(-30px);
      }
    }
    @keyframes fadeUp {
      to {
        opacity: 1;
        transform: translateY(0);
      }
      from {
        opacity: 0;
        transform: translateY(30px);
      }
    }
    @keyframes glowText {
      0%, 100% {
        text-shadow: 0 0 10px #00ff99, 0 0 20px #00ff99, 0 0 40px #00ff99;
      }
      50% {
        text-shadow: 0 0 20px #00ff99, 0 0 40px #00ff99, 0 0 80px #00ff99;
      }
    }
    @keyframes float {
      0%, 100% {
        transform: translateY(0) rotateY(0deg);
      }
      50% {
        transform: translateY(-20px) rotateY(10deg);
      }
    }
    @keyframes pulseContact {
      0% {
        box-shadow: 0 0 30px #00ff99;
      }
      100% {
        box-shadow: 0 0 50px #00ff99;
      }
    }

    /* Responsive */
    @media (max-width: 900px) {
      .hero {
        flex-direction: column;
      }
      .hero-text {
        padding-right: 0;
        text-align: center;
      }
      .hero-image {
        margin-top: 40px;
      }
    }
  </style>
</head>
<body>

  <header>
    <h1>SLG LED WALLS</h1>
    <p>Brighten Your Events with Cutting-Edge LED Technology</p>
  </header>

  <section class="container hero">
    <div class="hero-text">
      <h2>High-Definition LED Displays</h2>
      <p>
        Experience crystal clear visuals with our ultra-HD LED walls, perfect for concerts, weddings, corporate events, and more.
        We offer customizable sizes, fast setup, and unmatched brightness.
      </p>
      <button onclick="contactOwner()">Contact Suresh Now</button>
    </div>
    <div class="hero-image" aria-label="SLG LED Walls Display">
      <img src="https://images.unsplash.com/photo-1565372917903-02eeac157c7a?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="SLG LED Walls Display" />
    </div>
  </section>

  <section class="container features">
    <h3>Why Choose SLG LED Walls?</h3>
    <div class="feature-list">
      <div class="feature">
        <h4>Ultra HD Quality</h4>
        <p>Vivid colors and sharp images with advanced LED technology.</p>
      </div>
      <div class="feature">
        <h4>Custom Sizes</h4>
        <p>From small indoor panels to massive outdoor walls tailored to your needs.</p>
      </div>
      <div class="feature">
        <h4>Fast Setup</h4>
        <p>Professional installation team ready to deploy anywhere, anytime.</p>
      </div>
      <div class="feature">
        <h4>Reliable Support</h4>
        <p>Dedicated support and maintenance for flawless performance.</p>
      </div>
    </div>
  </section>

  <section class="container contact" id="contact-section">
    <h3>Contact Suresh - Owner & Managing Director</h3>
    <p>Ready to light up your next event? Reach out now!</p>
    <a href="tel:+919908395183" aria-label="Call Suresh at 9908395183">📞 Call: 9908395183</a>
  </section>

  <!-- Fixed contact button -->
  <div class="contact-fixed" role="button" aria-label="Call Suresh" tabindex="0" onclick="contactOwner()" onkeypress="if(event.key==='Enter'){contactOwner()}">
    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
      <path d="M6.62 10.79a15.09 15.09 0 006.59 6.59l2.2-2.2a1 1 0 011.11-.21 11.36 11.36 0 003.55.57 1 1 0 011 1v3.59a1 1 0 01-1 1A16 16 0 014 6a1 1 0 011-1h3.59a1 1 0 011 1 11.36 11.36 0 00.57 3.55 1 1 0 01-.21 1.11z"/>
    </svg>
  </div>

  <script>
    function contactOwner() {
      window.location.href = "tel:+919908395183";
    }
  </script>
</body>
</html>
