# COMMNS-OPEN-SPA
Comisiones ESPAÑOL
<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Mi Carrd - Ilustraciones</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Quicksand:wght@400;600;700&family=Patrick+Hand&display=swap');

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    font-family: 'Quicksand', sans-serif;
    background: repeating-linear-gradient(
      45deg,
      #f0e6f6,
      #f0e6f6 20px,
      #e6f9f0 20px,
      #e6f9f0 40px
    );
    min-height: 100vh;
    display: flex;
    justify-content: center;
    padding: 20px;
  }

  .carrd-container {
    width: 100%;
    max-width: 700px;
    background: #fff;
    border-radius: 20px;
    overflow: hidden;
    box-shadow: 0 8px 30px rgba(0,0,0,0.15);
    border: 3px dashed #a8d8b9;
  }

  /* HEADER */
  .header {
    background: linear-gradient(135deg, #a8d8b9, #f4b6c2);
    padding: 15px 20px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    color: #fff;
    font-size: 14px;
  }
  .header-left { display: flex; align-items: center; gap: 8px; }
  .header-right { display: flex; gap: 12px; align-items: center; }

  /* HERO / BANNER */
  .hero {
    background: linear-gradient(135deg, #fce4ec, #e0f2e9);
    padding: 25px;
    display: flex;
    gap: 20px;
    align-items: center;
    border-bottom: 3px dashed #f4b6c2;
  }
  .profile-pic {
    width: 110px;
    height: 110px;
    border-radius: 20px;
    border: 3px solid #fff;
    box-shadow: 0 4px 10px rgba(0,0,0,0.1);
    object-fit: cover;
    background: #fff;
  }
  .hero-text h1 {
    font-family: 'Patrick Hand', cursive;
    font-size: 28px;
    color: #5a3e5a;
    margin-bottom: 5px;
  }
  .hero-text p {
    color: #7a6a7a;
    font-size: 15px;
  }
  .speech-bubble {
    background: #fff;
    padding: 10px 18px;
    border-radius: 20px;
    border: 2px dashed #f4b6c2;
    font-family: 'Patrick Hand', cursive;
    color: #5a3e5a;
    margin-top: 8px;
    display: inline-block;
  }

  /* NAV BUTTONS */
  .nav-buttons {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    padding: 20px 25px;
    background: #fce4ec;
    justify-content: center;
    border-bottom: 3px dashed #a8d8b9;
  }
  .nav-btn {
    padding: 12px 22px;
    border-radius: 30px;
    border: 2px dashed #5a3e5a;
    background: #fff;
    font-family: 'Quicksand', sans-serif;
    font-weight: 700;
    font-size: 15px;
    color: #5a3e5a;
    cursor: pointer;
    text-decoration: none;
    transition: all 0.3s;
    display: flex;
    align-items: center;
    gap: 6px;
  }
  .nav-btn:hover {
    background: #a8d8b9;
    color: #fff;
    transform: translateY(-2px);
  }
  .nav-btn.green { background: #e0f2e9; }
  .nav-btn.pink { background: #fce4ec; }

  /* ABOUT SECTION */
  .section {
    padding: 25px;
    margin: 15px;
    background: #fff;
    border-radius: 18px;
    border: 2px dashed #a8d8b9;
  }
  .section-title {
    font-family: 'Patrick Hand', cursive;
    font-size: 24px;
    color: #5a3e5a;
    text-align: center;
    margin-bottom: 15px;
    background: linear-gradient(90deg, #e0f2e9, #fce4ec);
    padding: 10px;
    border-radius: 30px;
    border: 2px dashed #f4b6c2;
  }

  .about-content {
    display: flex;
    gap: 20px;
    align-items: flex-start;
  }
  .about-img {
    width: 160px;
    height: 160px;
    border-radius: 18px;
    border: 3px solid #a8d8b9;
    object-fit: cover;
    flex-shrink: 0;
  }
  .about-text h2 {
    font-family: 'Patrick Hand', cursive;
    font-size: 26px;
    color: #5a3e5a;
    margin-bottom: 5px;
  }
  .about-text .subtitle {
    color: #f4b6c2;
    font-weight: 700;
    margin-bottom: 10px;
  }
  .about-text p {
    color: #6a5a6a;
    font-size: 14px;
    line-height: 1.6;
  }

  /* STATUS */
  .status-box {
    background: #f9f9f9;
    padding: 15px 20px;
    border-radius: 15px;
    border: 2px dashed #f4b6c2;
    margin-top: 15px;
  }
  .status-item {
    display: flex;
    align-items: center;
    gap: 10px;
    margin: 8px 0;
    font-size: 15px;
  }
  .status-dot {
    width: 12px;
    height: 12px;
    border-radius: 50%;
    background: #a8d8b9;
  }
  .status-label {
    font-weight: 700;
    color: #5a3e5a;
    min-width: 100px;
  }

  /* GALLERY */
  .gallery-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 12px;
    margin-top: 15px;
  }
  .gallery-item {
    aspect-ratio: 1;
    border-radius: 15px;
    border: 3px solid #f4b6c2;
    overflow: hidden;
    cursor: pointer;
    transition: transform 0.3s;
  }
  .gallery-item:hover { transform: scale(1.05); }
  .gallery-item img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }

  /* DO / DON'T */
  .do-dont {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 15px;
    margin-top: 15px;
  }
  .do-box, .dont-box {
    padding: 15px;
    border-radius: 15px;
    border: 2px dashed;
  }
  .do-box { background: #e0f2e9; border-color: #a8d8b9; }
  .dont-box { background: #fce4ec; border-color: #f4b6c2; }
  .do-box h3, .dont-box h3 {
    font-family: 'Patrick Hand', cursive;
    font-size: 20px;
    margin-bottom: 10px;
  }
  .do-box h3 { color: #4a8a5a; }
  .dont-box h3 { color: #c25a6a; }
  .do-box ul, .dont-box ul {
    list-style: none;
    font-size: 14px;
    color: #5a4a5a;
  }
  .do-box li::before { content: "✅ "; }
  .dont-box li::before { content: "❌ "; }

  /* PRICE CARDS */
  .price-category {
    margin-bottom: 25px;
  }
  .price-category:last-child {
    margin-bottom: 0;
  }
  .price-category-title {
    font-family: 'Patrick Hand', cursive;
    font-size: 22px;
    margin-bottom: 12px;
    text-align: center;
  }
  .price-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 12px;
  }
  .price-card {
    padding: 15px;
    border-radius: 15px;
    border: 2px dashed;
    text-align: center;
    transition: transform 0.3s;
  }
  .price-card:hover {
    transform: translateY(-3px);
  }
  .price-card.green {
    background: #e0f2e9;
    border-color: #a8d8b9;
  }
  .price-card.pink {
    background: #fce4ec;
    border-color: #f4b6c2;
  }
  .price-card .type {
    font-size: 14px;
    color: #5a3e5a;
    margin-bottom: 8px;
  }
  .price-card .amount {
    font-size: 24px;
    font-weight: 700;
  }
  .price-card.green .amount { color: #4a8a5a; }
  .price-card.pink .amount { color: #c25a6a; }

  /* LINKS */
  .links-section {
    background: linear-gradient(135deg, #e0f2e9, #fce4ec);
    padding: 20px 25px;
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    justify-content: center;
    align-items: center;
  }
  .links-label {
    font-family: 'Patrick Hand', cursive;
    font-size: 22px;
    color: #5a3e5a;
    background: #fff;
    padding: 10px 20px;
    border-radius: 30px;
    border: 2px dashed #5a3e5a;
  }
  .social-btn {
    width: 45px;
    height: 45px;
    border-radius: 12px;
    border: 2px solid #fff;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 20px;
    text-decoration: none;
    transition: transform 0.3s;
    background: #fff;
  }
  .social-btn:hover { transform: translateY(-3px); }
  .social-btn.t { background: #fce4ec; }
  .social-btn.tw { background: #e0f2e9; }
  .social-btn.w { background: #fce4ec; }
  .social-btn.yt { background: #e0f2e9; }
  .social-btn.ig { background: #fce4ec; }
  .social-btn.tk { background: #e0f2e9; }
  .social-btn.dc { background: #fce4ec; }

  /* FOOTER */
  .footer {
    background: #5a3e5a;
    color: #fff;
    text-align: center;
    padding: 12px;
    font-size: 13px;
  }

  /* BANNER DECORATIVO */
  .banner-strip {
    height: 8px;
    background: repeating-linear-gradient(
      90deg,
      #a8d8b9 0px, #a8d8b9 20px,
      #f4b6c2 20px, #f4b6c2 40px
    );
  }

  /* Responsive */
  @media (max-width: 600px) {
    .about-content { flex-direction: column; align-items: center; text-align: center; }
    .gallery-grid { grid-template-columns: repeat(2, 1fr); }
    .price-grid { grid-template-columns: 1fr; }
    .do-dont { grid-template-columns: 1fr; }
    .hero { flex-direction: column; text-align: center; }
  }
</style>
</head>
<body>

<div class="carrd-container">

  <!-- HEADER -->
  <div class="header">
    <div class="header-left">
      <span>🌸</span>
      <span>by tu-nombre.carrd.co (✿◠‿◠)</span>
    </div>
    <div class="header-right">
      <span>🔖</span>
      <span>⏻</span>
      <span>✉</span>
      <span id="clock">10:23 pm</span>
    </div>
  </div>

  <div class="banner-strip"></div>

  <!-- HERO / BANNER PRINCIPAL -->
  <div class="hero">
    <!-- EDITAR: Cambia la URL de tu foto de perfil aquí -->
    <img src="https://via.placeholder.com/200x200/f4b6c2/fff?text=TU+FOTO" 
         alt="Foto de perfil" class="profile-pic" id="profilePic">
    <div class="hero-text">
      <h1>✧ Tu Nombre Artístico ✧</h1>
      <p>Ilustradora / Artista Digital</p>
      <div class="speech-bubble">(✿◠‿◠) ¡Bienvenidx a mi carrd!</div>
    </div>
  </div>

  <!-- BOTONES DE NAVEGACIÓN -->
  <div class="nav-buttons">
    <a href="#about" class="nav-btn green">🏠 About</a>
    <a href="#prices" class="nav-btn pink">💰 Precios</a>
    <a href="#tat" class="nav-btn green">⏱ TAT</a>
    <a href="#tos" class="nav-btn pink">📋 TOS</a>
    <a href="#gallery" class="nav-btn green">🌸 Galería</a>
    <a href="#do-dont" class="nav-btn pink">🎨 Do / Don't</a>
  </div>

  <!-- ABOUT ME -->
  <div class="section" id="about">
    <div class="section-title">✿ about me ✿</div>
    <div class="about-content">
      <!-- EDITAR: Imagen de tu personaje/avatar -->
      <img src="https://via.placeholder.com/200x200/a8d8b9/fff?text=AVATAR" 
           alt="Avatar" class="about-img">
      <div class="about-text">
        <!-- EDITAR: Tu nombre y descripción -->
        <h2>Tu Nombre ✦ Artista</h2>
        <p class="subtitle">info / info / info</p>
        <p>
          ¡Hola! Soy una ilustradora apasionada por crear personajes kawaii 
          y escenas mágicas. Me especializo en arte digital con colores pastel. 
          ¡Acepto commissions! 🌸
        </p>
      </div>
    </div>

    <!-- STATUS -->
    <div class="status-box">
      <div class="status-item">
        <div class="status-dot"></div>
        <span class="status-label">COMMS:</span>
        <span><!-- EDITAR --> Abiertos ✨</span>
      </div>
      <div class="status-item">
        <div class="status-dot"></div>
        <span class="status-label">TRADES:</span>
        <span><!-- EDITAR --> Cerrados</span>
      </div>
      <div class="status-item">
        <div class="status-dot"></div>
        <span class="status-label">REQUESTS:</span>
        <span><!-- EDITAR --> Cerrados</span>
      </div>
    </div>
  </div>

  <!-- 💰 PRECIOS ACTUALIZADOS 💰 -->
  <div class="section" id="prices">
    <div class="section-title">💰 precios / prices 💰</div>

    <!-- SKETCH -->
    <div class="price-category">
      <h3 class="price-category-title" style="color:#4a8a5a;">✏️ Sketch</h3>
      <div class="price-grid">
        <div class="price-card green">
          <p class="type">Icon</p>
          <p class="amount">$5 USD</p>
        </div>
        <div class="price-card green">
          <p class="type">Half Body</p>
          <p class="amount">$8 USD</p>
        </div>
        <div class="price-card green">
          <p class="type">Full Body</p>
          <p class="amount">$10 USD</p>
        </div>
      </div>
    </div>

    <!-- BASE COLOR -->
    <div class="price-category">
      <h3 class="price-category-title" style="color:#c25a6a;">🎨 Base Color</h3>
      <div class="price-grid">
        <div class="price-card pink">
          <p class="type">Icon</p>
          <p class="amount">$10 USD</p>
        </div>
        <div class="price-card pink">
          <p class="type">Half Body</p>
          <p class="amount">$15 USD</p>
        </div>
        <div class="price-card pink">
          <p class="type">Full Body</p>
          <p class="amount">$20 USD</p>
        </div>
      </div>
    </div>

    <!-- FULL RENDER -->
    <div class="price-category">
      <h3 class="price-category-title" style="color:#4a8a5a;">✨ Full Render</h3>
      <div class="price-grid">
        <div class="price-card green">
          <p class="type">Icon</p>
          <p class="amount">$15 USD</p>
        </div>
        <div class="price-card green">
          <p class="type">Half Body</p>
          <p class="amount">$25 USD</p>
        </div>
        <div class="price-card green">
          <p class="type">Full Body</p>
          <p class="amount">$30 USD</p>
        </div>
      </div>
    </div>

  </div>

  <!-- TAT -->
  <div class="section" id="tat">
    <div class="section-title">⏱ TAT (Tiempo de entrega) ⏱</div>
    <div style="background:#f9f9f9; padding:15px; border-radius:15px; border:2px dashed #a8d8b9; margin-top:10px;">
      <!-- EDITAR: Tus tiempos -->
      <p style="margin:8px 0;">🌸 <b>Sketch:</b> 1-2 días</p>
      <p style="margin:8px 0;">🌸 <b>Base Color:</b> 3-5 días</p>
      <p style="margin:8px 0;">🌸 <b>Full Render:</b> 5-7 días</p>
      <p style="margin-top:12px; font-size:13px; color:#888;">* Los tiempos pueden variar según la complejidad y mi carga de trabajo.</p>
    </div>
  </div>

  <!-- TOS -->
  <div class="section" id="tos">
    <div class="section-title">📋 TOS (Términos de servicio) 📋</div>
    <div style="background:#f9f9f9; padding:15px; border-radius:15px; border:2px dashed #f4b6c2; margin-top:10px; font-size:14px; line-height:1.8; color:#5a4a5a;">
      <!-- EDITAR: Tus términos -->
      <p>1. El pago se realiza <b>50% al inicio</b> y 50% al finalizar.</p>
      <p>2. Se permiten <b>2 revisiones gratuitas</b> por comisión.</p>
      <p>3. No se hacen reembolsos una vez iniciado el trabajo.</p>
      <p>4. El arte es para <b>uso personal</b> únicamente.</p>
      <p>5. Se dará crédito al artista al publicar la obra.</p>
      <p>6. Me reservo el derecho de rechazar cualquier solicitud.</p>
    </div>
  </div>

  <!-- GALERÍA -->
  <div class="section" id="gallery">
    <div class="section-title">🌸 galería / gallery 🌸</div>
    <div class="gallery-grid">
      <!-- EDITAR: Cambia las URLs por tus ilustraciones -->
      <div class="gallery-item"><img src="https://via.placeholder.com/200x200/f4b6c2/fff?text=Art+1" alt="Ilustración 1"></div>
      <div class="gallery-item"><img src="https://via.placeholder.com/200x200/a8d8b9/fff?text=Art+2" alt="Ilustración 2"></div>
      <div class="gallery-item"><img src="https://via.placeholder.com/200x200/fce4ec/5a3e5a?text=Art+3" alt="Ilustración 3"></div>
      <div class="gallery-item"><img src="https://via.placeholder.com/200x200/e0f2e9/5a3e5a?text=Art+4" alt="Ilustración 4"></div>
      <div class="gallery-item"><img src="https://via.placeholder.com/200x200/f4b6c2/fff?text=Art+5" alt="Ilustración 5"></div>
      <div class="gallery-item"><img src="https://via.placeholder.com/200x200/a8d8b9/fff?text=Art+6" alt="Ilustración 6"></div>
    </div>
  </div>

  <!-- DO / DON'T -->
  <div class="section" id="do-dont">
    <div class="section-title">🎨 lo que dibujo / lo que no 🎨</div>
    <div class="do-dont">
      <div class="do-box">
        <h3>✅ SÍ dibujo</h3>
        <ul>
          <!-- EDITAR -->
          <li>Personajes originales</li>
          <li>Fanart</li>
          <li>Furry / Anthro</li>
          <li>Chibis</li>
          <li>Escenas simples</li>
          <li>OCs</li>
        </ul>
      </div>
      <div class="dont-box">
        <h3>❌ NO dibujo</h3>
        <ul>
          <!-- EDITAR -->
          <li>NSFW / Gore</li>
          <li>Arte realista</li>
          <li>Mecha complejo</li>
          <li>Política</li>
          <li>Odio / discriminación</li>
          <li>IA / NFTs</li>
        </ul>
      </div>
    </div>
  </div>

  <!-- BANNER DECORATIVO -->
  <div class="banner-strip"></div>

  <!-- LINKS / REDES SOCIALES -->
  <div class="links-section">
    <div class="links-label">links</div>
    <!-- EDITAR: Cambia los # por tus URLs reales -->
    <a href="#" class="social-btn t" title="Tumblr">📝</a>
    <a href="#" class="social-btn tw" title="Twitter/X">🐦</a>
    <a href="#" class="social-btn w" title="Website">🌐</a>
    <a href="#" class="social-btn yt" title="YouTube">▶</a>
    <a href="#" class="social-btn ig" title="Instagram">📷</a>
    <a href="#" class="social-btn tk" title="TikTok">🎵</a>
    <a href="#" class="social-btn dc" title="Discord">💬</a>
  </div>

  <!-- FOOTER -->
  <div class="footer">
    ( Made with 💚 by Tu Nombre )
  </div>

</div>

<script>
  // Reloj en tiempo real
  function updateClock() {
    const now = new Date();
    let h = now.getHours();
    const m = String(now.getMinutes()).padStart(2, '0');
    const ampm = h >= 12 ? 'pm' : 'am';
    h = h % 12 || 12;
    document.getElementById('clock').textContent = `${h}:${m} ${ampm}`;
  }
  updateClock();
  setInterval(updateClock, 1000);

  // Scroll suave para los botones
  document.querySelectorAll('.nav-btn').forEach(btn => {
    btn.addEventListener('click', function(e) {
      const href = this.getAttribute('href');
      if (href.startsWith('#')) {
        e.preventDefault();
        document.querySelector(href).scrollIntoView({ behavior: 'smooth' });
      }
    });
  });
</script>

</body>
</html>
