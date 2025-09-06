# Chanelpty<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>chanelpty Premium</title>

  <!-- Google Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap" rel="stylesheet">

  <style>
    * { margin:0; padding:0; box-sizing:border-box; }
    body { font-family: 'Poppins', sans-serif; background:#fff; color:#111; }

    /* Header */
    header {
      background: url('https://images.unsplash.com/photo-1600181953130-d1a9e621f0b4?auto=format&fit=crop&w=1950&q=80') center/cover no-repeat;
      height: 350px;
      display: flex;
      justify-content: center;
      align-items: center;
      color: #fff;
      position: relative;
      text-align: center;
    }
    header::after {
      content:'';
      position:absolute;
      top:0; left:0; right:0; bottom:0;
      background:rgba(0,0,0,0.5);
    }
    header h1 {
      position: relative;
      font-size:3em;
      font-weight:700;
      z-index:1;
      text-shadow: 2px 2px 6px rgba(0,0,0,0.7);
    }

    /* Hero */
    .hero { padding:40px 20px; text-align:center; background:#fff5fa; }
    .hero h2 { font-size:2em; margin-bottom:10px; color:#d63384; }
    .hero p { font-size:1.1em; color:#555; }

    /* Slider */
    .slider-container {
      position: relative;
      max-width: 900px;
      margin: 40px auto;
      overflow: hidden;
      border-radius:15px;
    }
    .slider {
      display: flex;
      transition: transform 0.5s ease-in-out;
    }
    .card {
      min-width: 250px;
      margin: 20px;
      background:#fff;
      border-radius:15px;
      padding:20px;
      text-align:center;
      box-shadow:0 8px 15px rgba(0,0,0,0.1);
      transition: transform 0.3s ease, box-shadow 0.3s ease;
    }
    .card:hover { transform: translateY(-5px); box-shadow:0 12px 20px rgba(0,0,0,0.2); }
    .card h3 { margin:10px 0 5px; font-size:1.2em; color:#333; }
    .price { color:#d63384; font-weight:700; margin-bottom:15px; font-size:1.1em; }
    .btn { background:#d63384; color:#fff; border:none; padding:12px 25px; border-radius:50px; cursor:pointer; font-weight:600; font-size:1em; transition: background 0.3s ease, transform 0.2s ease; }
    .btn:hover { background:#b52b6d; transform: scale(1.05); }

    /* Slider buttons */
    .prev, .next {
      position: absolute;
      top:50%;
      transform: translateY(-50%);
      background: rgba(0,0,0,0.5);
      color:#fff;
      border:none;
      padding:10px;
      border-radius:50%;
      cursor:pointer;
      font-size:1.2em;
      z-index:1;
    }
    .prev { left:10px; }
    .next { right:10px; }

    /* Testimonios */
    .testimonials {
      background:#fff5fa;
      padding:40px 20px;
      text-align:center;
    }
    .testimonials h2 { font-size:2em; margin-bottom:20px; color:#d63384; }
    .testimonial { max-width:700px; margin:20px auto; font-style:italic; color:#555; }

    /* Contacto */
    .contact {
      padding:40px 20px;
      text-align:center;
    }
    .contact h2 { font-size:2em; margin-bottom:20px; color:#d63384; }
    .contact form {
      max-width:500px;
      margin:0 auto;
      display:flex;
      flex-direction:column;
      gap:15px;
    }
    .contact input, .contact textarea {
      padding:12px;
      border-radius:8px;
      border:1px solid #ddd;
      font-size:1em;
      width:100%;
    }
    .contact button { align-self:center; }

    /* Footer */
    footer { text-align:center; padding:20px; background:#ffeef8; font-size:0.9em; }
    footer a { color:#d63384; text-decoration:none; font-weight:600; }
    footer a:hover { text-decoration:underline; }

    /* Responsive */
    @media (max-width:700px) {
      .card { min-width:200px; margin:10px; }
      header h1 { font-size:2.2em; }
    }
  </style>
</head>
<body>

  <header>
    <h1>chanelpty</h1>
  </header>

  <section class="hero">
    <h2>Perfumes, Labiales, Shampoos y Cremas</h2>
    <p>Productos seleccionados con cariño para ti ✨</p>
  </section>

  <!-- Slider de productos -->
  <section class="slider-container">
    <button class="prev">&#10094;</button>
    <div class="slider">
      <div class="card">
        <h3>Perfume Floral</h3>
        <p class="price">$28.00</p>
        <button class="btn" onclick="openWhatsApp('Perfume Floral')">Comprar</button>
      </div>
      <div class="card">
        <h3>Labial Mate</h3>
        <p class="price">$9.50</p>
        <button class="btn" onclick="openWhatsApp('Labial Mate')">Comprar</button>
      </div>
      <div class="card">
        <h3>Shampoo Nutritivo</h3>
        <p class="price">$12.00</p>
        <button class="btn" onclick="openWhatsApp('Shampoo Nutritivo')">Comprar</button>
      </div>
      <div class="card">
        <h3>Crema Hidratante</h3>
        <p class="price">$14.00</p>
        <button class="btn" onclick="openWhatsApp('Crema Hidratante')">Comprar</button>
      </div>
      <div class="card">
        <h3>Perfume Rosado</h3>
        <p class="price">$30.00</p>
        <button class="btn" onclick="openWhatsApp('Perfume Rosado')">Comprar</button>
      </div>
    </div>
    <button class="next">&#10095;</button>
  </section>

  <!-- Testimonios -->
  <section class="testimonials">
    <h2>Lo que dicen nuestros clientes</h2>
    <p class="testimonial">"¡Los productos son increíbles! La entrega fue rápida y todo llegó perfecto." – Ana G.</p>
    <p class="testimonial">"Me encantó el labial, dura mucho y el color es hermoso." – Carla R.</p>
  </section>

  <!-- Contacto -->
  <section class="contact">
    <h2>Contáctanos</h2>
    <form onsubmit="alert('Formulario enviado!'); return false;">
      <input type="text" placeholder="Nombre" required>
      <input type="email" placeholder="Correo" required>
      <textarea placeholder="Mensaje" rows="4" required></textarea>
      <button class="btn" type="submit">Enviar</button>
    </form>
  </section>

  <footer>
    📞 <a href="tel:+50764446030">+507 6444-6030</a> • 
    📸 <a href="https://instagram.com/chanelquintero" target="_blank">@chanelquintero</a>
  </footer>

  <script>
    // Slider automático y manual
    const slider = document.querySelector('.slider');
    const slides = document.querySelectorAll('.slider .card');
    const prev = document.querySelector('.prev');
    const next = document.querySelector('.next');
    let index = 0;

    function showSlide(i){
      const width = slides[0].offsetWidth + 40;
      if(i < 0) index = slides.length - 1;
      else if(i >= slides.length) index = 0;
      else index = i;
      slider.style.transform = `translateX(${-index * width}px)`;
    }

    prev.addEventListener('click', () => showSlide(index - 1));
    next.addEventListener('click', () => showSlide(index + 1));
    window.addEventListener('resize', () => showSlide(index));

    // Animación automática
    setInterval(() => showSlide(index + 1), 4000); // cambia cada 4s

    // WhatsApp directo
    function openWhatsApp(product){
      const phone = "+50764446030";
      const text = encodeURIComponent(`Hola, quiero comprar: ${product}`);
      window.open(`https://wa.me/${phone}?text=${text}`, '_blank');
    }

    showSlide(index);
  </script>

</body>
</html>
