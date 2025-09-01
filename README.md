
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=no" />
  <title>Carta de Amor - 2025</title>

  <!-- Google Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@700&family=Playfair+Display:wght@700&family=Poppins:wght@400;500&display=swap" rel="stylesheet">

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Poppins', sans-serif;
      background: #fffaf9;
      color: #555;
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      padding: 20px;
      overflow-x: hidden;
      position: relative;
    }

    /* Animación de borde brillante sutil (solo líneas brillantes) */
    @keyframes rainbowGlow {
      0% { box-shadow: 0 0 12px rgba(180, 50, 200, 0.4); }
      33% { box-shadow: 0 0 12px rgba(230, 80, 190, 0.4); }
      66% { box-shadow: 0 0 12px rgba(140, 100, 255, 0.4); }
      100% { box-shadow: 0 0 12px rgba(180, 50, 200, 0.4); }
    }

    /* Marco brillante solo en el borde */
    .glow-frame {
      position: relative;
      display: inline-block;
      border-radius: 18px;
      margin: 1.4rem 0;
      animation: rainbowGlow 3s ease-in-out infinite alternate;
      padding: 3px;
      background: linear-gradient(45deg, #ba68c8, #e91e63, #7b1fa2, #ec407a);
    }

    .glow-frame img {
      border-radius: 15px;
      display: block;
      width: 100%;
      height: auto;
      border: 4px solid #fff;
      transition: transform 0.3s ease;
    }

    .glow-frame img:hover {
      transform: scale(1.03);
    }

    /* Botón del menú (3 rayitas) */
    .menu-btn {
      position: absolute;
      top: 20px;
      left: 20px;
      width: 50px;
      height: 50px;
      background: rgba(123, 31, 162, 0.1);
      border-radius: 50%;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      cursor: pointer;
      z-index: 100;
      box-shadow: 0 2px 8px rgba(0, 0, 0, 0.08);
      transition: all 0.3s;
    }

    .menu-btn span {
      display: block;
      width: 24px;
      height: 3px;
      background: #9c27b0;
      margin: 3px 0;
      border-radius: 2px;
    }

    .menu-btn:hover {
      background: rgba(123, 31, 162, 0.15);
      transform: scale(1.05);
    }

    /* Menú desplegable */
    .menu {
      position: fixed;
      top: 0;
      left: -300px;
      width: 280px;
      height: 100vh;
      background: rgba(255, 255, 255, 0.98);
      backdrop-filter: blur(10px);
      box-shadow: 0 0 30px rgba(0, 0, 0, 0.12);
      padding: 60px 20px 20px;
      transition: left 0.4s ease;
      z-index: 99;
      border-radius: 0 20px 20px 0;
      border-left: 2px solid #9c27b0;
    }

    .menu.open {
      left: 0;
    }

    .menu h3 {
      font-family: 'Playfair Display', serif;
      color: #8e24aa;
      margin-bottom: 1.2rem;
      font-size: 1.4rem;
      border-bottom: 1px solid #d1c4e9;
      padding-bottom: 0.5rem;
    }

    .menu p {
      color: #666;
      font-size: 0.95rem;
      line-height: 1.6;
      margin-bottom: 1.4rem;
    }

    .whatsapp-btn {
      display: block;
      margin: 1.5rem auto;
      padding: 1rem 1.4rem;
      background: linear-gradient(45deg, #25D366, #128C7E);
      color: white;
      text-align: center;
      border-radius: 14px;
      text-decoration: none;
      font-weight: 500;
      font-size: 1.05rem;
      box-shadow: 0 6px 15px rgba(37, 211, 102, 0.4);
      transition: all 0.3s;
    }

    .whatsapp-btn:hover {
      transform: scale(1.05);
      box-shadow: 0 8px 20px rgba(37, 211, 102, 0.5);
    }

    .close-menu {
      position: absolute;
      top: 20px;
      right: 20px;
      font-size: 1.5rem;
      color: #8e24aa;
      cursor: pointer;
    }

    /* Pantalla de bloqueo - diseño muy suave */
    .lock-screen {
      text-align: center;
      padding: 2rem;
      max-width: 440px;
      background: rgba(255, 255, 255, 0.9);
      border-radius: 24px;
      box-shadow: 0 4px 20px rgba(0, 0, 0, 0.06);
      border: 1px solid #eee;
      position: relative;
      z-index: 1;
    }

    .lock-screen h2 {
      font-family: 'Playfair Display', serif;
      font-size: 2rem;
      color: #6a1b9a;
      margin: 1.2rem 0;
    }

    .lock-screen p {
      color: #777;
      font-size: 1.1rem;
      margin-bottom: 1.4rem;
      font-weight: 400;
    }

    /* Display de clave - fondo muy claro */
    .key-display {
      font-family: 'Poppins', monospace;
      font-size: 1.8rem;
      color: #8e24aa;
      background: #fcfbff;
      padding: 1rem 1.3rem;
      border-radius: 12px;
      margin: 1.3rem auto;
      width: 90%;
      border: 1px solid #e0e0e0;
      letter-spacing: 5px;
      box-shadow: 0 2px 8px rgba(142, 36, 170, 0.1);
    }

    /* Teclado - botones suaves */
    .keypad {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 12px;
      margin: 1.4rem 0;
    }

    .key {
      font-size: 1.45rem;
      font-weight: 600;
      padding: 1.1rem 0;
      background: #f9f7ff;
      color: #8e24aa;
      border: 1px solid #e0e0e0;
      border-radius: 12px;
      cursor: pointer;
      transition: all 0.2s ease;
    }

    .key:hover {
      background: #f3eaff;
      transform: translateY(-3px);
      box-shadow: 0 4px 10px rgba(142, 36, 170, 0.15);
    }

    .key:active {
      transform: translateY(-1px);
    }

    /* Botón Iniciar */
    .btn-iniciar {
      margin-top: 1.6rem;
      padding: 1rem 2.2rem;
      font-size: 1.3rem;
      font-weight: 600;
      background: linear-gradient(45deg, #8e24aa, #ba68c8);
      color: white;
      border: none;
      border-radius: 30px;
      cursor: pointer;
      box-shadow: 0 6px 16px rgba(142, 36, 170, 0.3);
      transition: all 0.3s ease;
    }

    .btn-iniciar:hover {
      transform: scale(1.06);
      box-shadow: 0 8px 20px rgba(142, 36, 170, 0.4);
    }

    /* Contenedor principal */
    .main-container {
      display: none;
      text-align: center;
      max-width: 95%;
      padding: 2rem 1.6rem;
    }

    .letter-frame {
      background: rgba(255, 255, 255, 0.95);
      border-radius: 24px;
      padding: 2.2rem 1.8rem;
      box-shadow: 0 6px 24px rgba(142, 36, 170, 0.12);
      position: relative;
      margin-bottom: 1.8rem;
    }

    .letter-frame::before {
      content: '';
      position: absolute;
      inset: 0;
      border-radius: 24px;
      padding: 3px;
      background: linear-gradient(45deg, #ba68c8, #8e24aa);
      -webkit-mask: linear-gradient(#fff 0 0) content-box, linear-gradient(#fff 0 0);
      -webkit-mask-composite: destination-out;
      mask-composite: subtract;
      pointer-events: none;
    }

    h1 {
      font-family: 'Playfair Display', serif;
      font-size: 2.3rem;
      background: linear-gradient(45deg, #8e24aa, #ba68c8);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      margin-bottom: 1.5rem;
    }

    .letter {
      font-family: 'Dancing Script', cursive;
      font-size: 1.6rem;
      line-height: 1.9;
      color: #6a1b9a;
      text-align: left;
      white-space: pre-line;
      letter-spacing: 0.8px;
      margin: 0;
      opacity: 1;
    }

    footer {
      margin-top: 1.6rem;
      font-style: italic;
      color: #9c27b0;
      font-size: 1.1rem;
    }

    /* Corazones flotantes */
    .floating-heart {
      position: fixed;
      font-size: 18px;
      pointer-events: none;
      opacity: 0;
      z-index: 1000;
      user-select: none;
      animation: floatUp 16s ease-out forwards, fadeHeart 4s ease-in-out infinite;
    }

    @keyframes floatUp {
      0% { transform: translateY(100vh) rotate(0deg); opacity: 0; }
      10% { opacity: 0.8; }
      90% { opacity: 0.8; }
      100% { transform: translateY(-15vh) rotate(360deg); opacity: 0; }
    }

    @keyframes fadeHeart {
      0%, 100% { opacity: 0.6; }
      50% { opacity: 1; }
    }

    /* Créditos */
    .credit {
      margin-top: 1.6rem;
      font-size: 0.75rem;
      color: #bbb;
      font-style: italic;
    }

    .credit strong {
      color: #8e24aa;
      font-weight: 600;
    }

    @media (max-width: 480px) {
      .lock-screen, .main-container {
        padding: 1.6rem;
        max-width: 98%;
      }

      h1 {
        font-size: 2rem;
      }

      .letter {
        font-size: 1.5rem;
        line-height: 1.8;
      }

      .btn-iniciar {
        font-size: 1.2rem;
        padding: 0.9rem 2rem;
      }
    }
  </style>
</head>
<body>

  <!-- Botón del menú (3 rayitas) -->
  <div class="menu-btn" onclick="toggleMenu()">
    <span></span>
    <span></span>
    <span></span>
  </div>

  <!-- Menú desplegable -->
  <div id="menu" class="menu">
    <div class="close-menu" onclick="toggleMenu()">✕</div>
    <h3>🛠️ Personalización</h3>
    <p>¿Quieres personalizar esta carta, el código de acceso o usar este diseño para tu proyecto?</p>
    <a href="https://wa.me/51937556459" target="_blank" class="whatsapp-btn">
      💬 Contactar por WhatsApp
    </a>
  </div>

  <!-- Pantalla de bloqueo -->
  <div id="lockScreen" class="lock-screen">
    <h2>🔐 Una Carta de Amor</h2>
    <p>👇INGRESA EL CÓDIGO DE ACCESO 👇</p>

    <div class="glow-frame">
      <img src="https://media2.giphy.com/media/v1.Y2lkPTZjMDliOTUyZTAxbHV0Mm1rYmI2emc3ZmdvcGdka2szMGMzMHl4ZXlhcmEzN3A4cCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/Y62ofc4S1Vst2/giphy.gif" alt="Corazones flotando" width="180" height="180" />
    </div>

    <div id="display" class="key-display"></div>

    <div class="keypad">
      <div class="key" onclick="addDigit('1')">1</div>
      <div class="key" onclick="addDigit('2')">2</div>
      <div class="key" onclick="addDigit('3')">3</div>
      <div class="key" onclick="addDigit('4')">4</div>
      <div class="key" onclick="addDigit('5')">5</div>
      <div class="key" onclick="addDigit('6')">6</div>
      <div class="key" onclick="addDigit('7')">7</div>
      <div class="key" onclick="addDigit('8')">8</div>
      <div class="key" onclick="addDigit('9')">9</div>
      <div class="key" onclick="addDigit('0')">0</div>
      <div class="key" onclick="clearInput()">⌫</div>
      <div class="key" onclick="clearInput()">Limpiar</div>
    </div>

    <button class="btn-iniciar" onclick="submitKey()">Iniciar</button>

    <div class="glow-frame">
      <img src="https://media0.giphy.com/media/v1.Y2lkPTZjMDliOTUyMzl0NTh2ZHhmOHF1Nm45NHNqcmN1bTVrdHNtbDgwbjZpZTFqMno3diZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/11TyfGbDbBv4be/giphy.gif" alt="Bailarina de amor" width="180" height="180" />
    </div>
  </div>

  <!-- Carta principal -->
  <div id="mainContainer" class="main-container">
    <div class="letter-frame">
      <h1>Para Ti, con Amor 💖</h1>
      <div id="letter" class="letter"></div>
      <footer>Con todo mi corazón, Te dedico ésto para usted.</footer>
    </div>

    <!-- GIF debajo de la carta con borde brillante -->
    <div class="glow-frame" style="margin-top: 1.6rem; max-width: 200px;">
      <img src="https://media0.giphy.com/media/v1.Y2lkPTZjMDliOTUyMzl0NTh2ZHhmOHF1Nm45NHNqcmN1bTVrdHNtbDgwbjZpZTFqMno3diZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/11TyfGbDbBv4be/giphy.gif" alt="Bailarina de amor" />
    </div>

    <p class="credit">By <strong>AnthZz Berrocal | BerMatMods</strong></p>
  </div>

  <script>
    let input = '';
    const correctKey = '2025';

    function addDigit(digit) {
      if (input.length < 4) {
        input += digit;
        updateDisplay();
      }
    }

    function clearInput() {
      input = '';
      updateDisplay();
    }

    function updateDisplay() {
      document.getElementById('display').textContent = input;
    }

    function submitKey() {
      if (input === correctKey) {
        document.getElementById('lockScreen').style.display = 'none';
        document.getElementById('mainContainer').style.display = 'block';
        typeWriter();
        createHearts();
      } else {
        alert('❌ Código incorrecto. Intenta de nuevo.');
        clearInput();
      }
    }

    function toggleMenu() {
      document.getElementById('menu').classList.toggle('open');
    }

    function createHearts() {
      const hearts = ['❤️', '💖', '💕', '💓', '💗', '💞', '💘'];
      setInterval(() => {
        const heart = document.createElement('div');
        heart.className = 'floating-heart';
        heart.textContent = hearts[Math.floor(Math.random() * hearts.length)];
        heart.style.left = Math.random() * 90 + 5 + 'vw';
        heart.style.bottom = '0';
        document.body.appendChild(heart);

        setTimeout(() => {
          heart.remove();
        }, 18000);
      }, 2800);
    }

    function typeWriter() {
      const letterElement = document.getElementById('letter');
      letterElement.textContent = '';
      letterElement.style.opacity = 1;

      const message = `En cada latido, pienso en ti.
No necesito palabras para decirte que eres mi todo,
porque mi corazón ya lo grita en silencio.

Desde el primer momento, supe que eras especial.
Tu presencia ilumina mis días,
tu sonrisa es mi refugio,
y tu amor, mi mayor milagro.

No hay distancia, ni tiempo,
ni universo que pueda separar lo que siento.
Eres mi sueño hecho realidad,
mi paz, mi locura, mi eternidad.

Gracias por existir,
por amar, por sonreír,
por ser tú.

Este momento, este amor,
es para ti.`;

      let i = 0;
      const speed = 40;

      function type() {
        if (i < message.length) {
          letterElement.textContent += message.charAt(i);
          i++;
          setTimeout(type, speed);
        }
      }

      setTimeout(type, 300);
    }
  </script>
</body>
</html>
