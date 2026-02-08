<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Sonvi</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, Helvetica, sans-serif;
      line-height: 1.6;
      background: #f5f7fb;
    }
    header {
      background: #0b5ed7;
      color: #fff;
      padding: 20px 40px;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    header h1 { margin: 0; }
    nav a {
      color: #fff;
      margin-left: 20px;
      text-decoration: none;
      font-weight: bold;
    }
    nav a:hover { text-decoration: underline; }

    .hero {
      background: url('https://images.unsplash.com/photo-1523050854058-8df90110c9f1') center/cover no-repeat;
      color: #fff;
      padding: 120px 40px;
      text-align: center;
    }
    .hero h2 { font-size: 42px; }
    .hero p { font-size: 20px; }

    section {
      padding: 60px 40px;
      background: #fff;
      margin-bottom: 20px;
    }
    section h2 { text-align: center; margin-bottom: 30px; }

    .courses, .gallery {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 20px;
    }
    .card {
      background: #f1f3f8;
      padding: 20px;
      border-radius: 8px;
      box-shadow: 0 2px 6px rgba(0,0,0,0.1);
    }
    .card img {
      width: 100%;
      border-radius: 6px;
    }

    .counter {
      font-size: 32px;
      color: #0b5ed7;
      font-weight: bold;
      text-align: center;
    }

    form {
      max-width: 500px;
      margin: auto;
    }
    form input, form textarea, form button {
      width: 100%;
      padding: 10px;
      margin: 10px 0;
    }
    form button {
      background: #0b5ed7;
      color: #fff;
      border: none;
      cursor: pointer;
    }

    footer {
      background: #222;
      color: #ccc;
      text-align: center;
      padding: 20px;
    }
  </style>
</head>
<body>

<header>
  <h1>Sonvi website</h1>
  <nav>
    <a href="#home">Home</a>
    <a href="#courses">Courses</a>
    <a href="#about">About</a>
    <a href="#contact">Contact</a>
  </nav>
</header>

<section class="hero" id="home">
  <h2>Build Your Career in Data & Cloud</h2>
  <p>Industry-focused training with real-time projects</p>
</section>

<section id="courses">
  <h2>Our Courses</h2>
  <div class="courses">
    <div class="card">
      <h3>Data Analytics</h3>
      <p>Excel, SQL, Power BI, Python</p>
    </div>
    <div class="card">
      <h3>Data Science</h3>
      <p>Python, ML, AI, Projects</p>
    </div>
    <div class="card">
      <h3>Cloud & DevOps</h3>
      <p>AWS, Azure, CI/CD</p>
    </div>
  </div>
</section>

<section id="about">
  <h2>Why Choose Us</h2>
  <p style="text-align:center">We focus on hands-on learning, real-time use cases, and placement support.</p>
  <div class="counter" id="students">0+ Students Trained</div>
</section>

<section>
  <h2>Gallery</h2>
  <div class="gallery">
    <div class="card"><img src="https://images.unsplash.com/photo-1522071820081-009f0129c71c" /></div>
    <div class="card"><img src="https://images.unsplash.com/photo-1556761175-4b46a572b786" /></div>
    <div class="card"><img src="https://images.unsplash.com/photo-1584697964154-38c7b7e5b8c2" /></div>
  </div>
</section>

<section id="contact">
  <h2>Contact Us</h2>
  <form onsubmit="sendMessage(event)">
    <input type="text" placeholder="Your Name" required />
    <input type="email" placeholder="Your Email" required />
    <textarea placeholder="Your Message"></textarea>
    <button type="submit">Send</button>
  </form>
</section>

<footer>
  <p>© 2026 Balachandra | All Rights Reserved</p>
</footer>

<script>
  let count = 0;
  let target = 1200;
  let counter = document.getElementById('students');
  let interval = setInterval(() => {
    count += 10;
    counter.innerText = count + '+ Students Trained';
    if (count >= target) clearInterval(interval);
  }, 20);

  function sendMessage(e) {
    e.preventDefault();
    alert('Thank you! We will contact you soon.');
  }
</script>

</body>
</html>
