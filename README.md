
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
      filter: saturate(1.6);
    }

    /* Animación de borde brillante súper intensa */
    @keyframes rainbowGlow {
      0% { box-shadow: 0 0 18px rgba(255, 0, 255, 0.7), 0 0 25px rgba(255, 100, 255, 0.6); }
      33% { box-shadow: 0 0 18px rgba(255, 100, 255, 0.7), 0 0 25px rgba(255, 0, 255, 0.6); }
      66% { box-shadow: 0 0 18px rgba(255, 0, 255, 0.7), 0 0 25px rgba(100, 0, 255, 0.6); }
      100% { box-shadow: 0 0 18px rgba(255, 0, 255, 0.7), 0 0 25px rgba(255, 100, 255, 0.6); }
    }

    .glow-frame {
      position: relative;
      display: inline-block;
      border-radius: 18px;
      margin: 1.4rem 0;
      animation: rainbowGlow 2s ease-in-out infinite alternate;
      padding: 3px;
      background: linear-gradient(45deg, #ff00ff, #ff00cc, #ff66ff, #ff33ff);
      overflow: visible;
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
      background: rgba(123, 31, 162, 0.15);
      border-radius: 50%;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      cursor: pointer;
      z-index: 100;
      box-shadow: 0 2px 10px rgba(142, 36, 170, 0.2);
      transition: all 0.3s;
    }

    .menu-btn span {
      display: block;
      width: 24px;
      height: 3px;
      background: #9c27b0;
      margin: 3px 0;
      border-radius: 2px;
      box-shadow: 0 0 8px rgba(156, 39, 176, 0.5);
    }

    .menu-btn:hover {
      background: rgba(123, 31, 162, 0.2);
      transform: scale(1.08);
    }

    /* Menú desplegable */
    .menu {
      position: fixed;
      top: 0;
      left: -300px;
      width: 280px;
      height: 100vh;
      background: rgba(255, 255, 255, 0.99);
      backdrop-filter: blur(12px);
      box-shadow: 0 0 35px rgba(142, 36, 170, 0.18);
      padding: 60px 20px 20px;
      transition: left 0.4s ease;
      z-index: 99;
      border-radius: 0 20px 20px 0;
      border-left: 3px solid #9c27b0;
    }

    .menu.open {
      left: 0;
    }

    .menu h3 {
      font-family: 'Playfair Display', serif;
      color: #8e24aa;
      margin-bottom: 1.2rem;
      font-size: 1.4rem;
      border-bottom: 1px solid #e1bee7;
      padding-bottom: 0.5rem;
    }

    .menu p {
      color: #555;
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
      box-shadow: 0 8px 20px rgba(37, 211, 102, 0.5);
      transition: all 0.3s;
    }

    .whatsapp-btn:hover {
      transform: scale(1.08);
      box-shadow: 0 10px 25px rgba(37, 211, 102, 0.6);
    }

    .close-menu {
      position: absolute;
      top: 20px;
      right: 20px;
      font-size: 1.5rem;
      color: #8e24aa;
      cursor: pointer;
    }

    /* Pantalla de bloqueo */
    .lock-screen {
      text-align: center;
      padding: 2rem;
      max-width: 440px;
      background: rgba(255, 255, 255, 0.95);
      border-radius: 24px;
      box-shadow: 0 6px 25px rgba(142, 36, 170, 0.1);
      border: 1px solid #ddd;
      position: relative;
      z-index: 1;
      overflow: visible;
    }

    .lock-screen h2 {
      font-family: 'Playfair Display', serif;
      font-size: 2rem;
      color: #6a1b9a;
      margin: 1.2rem 0;
      text-shadow: 0 0 8px rgba(255, 0, 255, 0.2);
    }

    .lock-screen p {
      color: #666;
      font-size: 1.1rem;
      margin-bottom: 1.4rem;
      font-weight: 400;
    }

    /* Display de clave */
    .key-display {
      font-family: 'Poppins', monospace;
      font-size: 1.8rem;
      color: #8e24aa;
      background: #fdfcff;
      padding: 1rem 1.3rem;
      border-radius: 12px;
      margin: 1.3rem auto;
      width: 90%;
      border: 1px solid #d0d0ff;
      letter-spacing: 5px;
      box-shadow: 0 3px 12px rgba(142, 36, 170, 0.15);
    }

    /* Teclado */
    .keypad {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 14px;
      margin: 1.4rem 0;
    }

    .key {
      font-size: 1.45rem;
      font-weight: 600;
      padding: 1.1rem 0;
      background: #f8f4ff;
      color: #8e24aa;
      border: 1px solid #d0d0ff;
      border-radius: 12px;
      cursor: pointer;
      transition: all 0.2s ease;
      box-shadow: 0 2px 6px rgba(142, 36, 170, 0.1);
    }

    .key:hover {
      background: #f0e6ff;
      transform: translateY(-4px);
      box-shadow: 0 6px 14px rgba(142, 36, 170, 0.2);
    }

    .key:active {
      transform: translateY(-2px);
    }

    /* Botón Iniciar */
    .btn-iniciar {
      margin-top: 1.6rem;
      padding: 1rem 2.2rem;
      font-size: 1.3rem;
      font-weight: 600;
      background: linear-gradient(45deg, #9c27b0, #d060ff);
      color: white;
      border: none;
      border-radius: 30px;
      cursor: pointer;
      box-shadow: 0 8px 20px rgba(156, 39, 176, 0.4);
      transition: all 0.3s ease;
    }

    .btn-iniciar:hover {
      transform: scale(1.08);
      box-shadow: 0 10px 25px rgba(156, 39, 176, 0.5);
    }

    /* Contenido principal */
    .main-container {
      display: none;
      text-align: center;
      max-width: 95%;
      padding: 2rem 1.6rem;
    }

    .letter-frame {
      background: rgba(255, 255, 255, 0.98);
      border-radius: 24px;
      padding: 2.2rem 1.8rem;
      box-shadow: 0 8px 30px rgba(142, 36, 170, 0.18);
      position: relative;
      margin-bottom: 1.8rem;
    }

    .letter-frame::before {
      content: '';
      position: absolute;
      inset: 0;
      border-radius: 24px;
      padding: 3px;
      background: linear-gradient(45deg, #d060ff, #9c27b0);
      -webkit-mask: linear-gradient(#fff 0 0) content-box, linear-gradient(#fff 0 0);
      -webkit-mask-composite: destination-out;
      mask-composite: subtract;
      pointer-events: none;
    }

    h1 {
      font-family: 'Playfair Display', serif;
      font-size: 2.3rem;
      background: linear-gradient(45deg, #9c27b0, #d060ff);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      margin-bottom: 1.5rem;
      text-shadow: 0 0 10px rgba(156, 39, 176, 0.2);
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
      font-size: 22px;
      pointer-events: none;
      opacity: 0;
      z-index: 1000;
      user-select: none;
      animation: floatUp 14s ease-out forwards, pulseHeart 3s ease-in-out infinite;
    }

    @keyframes floatUp {
      0% { transform: translateY(100vh) rotate(0deg); opacity: 0; }
      10% { opacity: 0.9; }
      90% { opacity: 0.9; }
      100% { transform: translateY(-20vh) rotate(360deg); opacity: 0; }
    }

    @keyframes pulseHeart {
      0%, 100% { transform: scale(1); }
      50% { transform: scale(1.15); }
    }

    /* Créditos */
    .credit {
      margin-top: 1.6rem;
      font-size: 0.75rem;
      color: #aaa;
      font-style: italic;
    }

    .credit strong {
      color: #9c27b0;
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
    <a href="https://wa.me/51930569195" target="_blank" class="whatsapp-btn">
      💬 Contactar por WhatsApp
    </a>
  </div>

  <!-- Pantalla de bloqueo -->
  <div id="lockScreen" class="lock-screen">
    <h2>🔐 Una Carta de Amor</h2>
    <p>👇INGRESA EL CÓDIGO DE ACCESO 👇</p>

    <div class="glow-frame">
      <img src="https://media2.giphy.com/media/v1.Y2lkPTZjMDliOTUyZTAxbHV0Mm1rYmI2emc3ZmdvcGdka2szMGMzMHl4ZXlhcmEzN3A4cCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/Y62ofc4S1Vst2/giphy.gif" alt="Corazones flotando" />
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
      <img src="https://media0.giphy.com/media/v1.Y2lkPTZjMDliOTUyMzl0NTh2ZHhmOHF1Nm45NHNqcmN1bTVrdHNtbDgwbjZpZTFqMno3diZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/11TyfGbDbBv4be/giphy.gif" alt="Bailarina de amor" />
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
    <div class="glow-frame" style="margin-top: 1.6rem;">
      <img src="https://media0.giphy.com/media/v1.Y2lkPTZjMDliOTUyMzl0NTh2ZHhmOHF1Nm45NHNqcmN1bTVrdHNtbDgwbjZpZTFqMno3diZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/11TyfGbDbBv4be/giphy.gif" alt="Bailarina de amor" />
    </div>

    <p class="credit">By <strong>AnthZz Berrocal | BerMatMods</strong></p>
  </div>

  <!-- Efecto táctil: explosión de corazones y chispas -->
  <script>
    function createTouchEffect(x, y) {
      const colors = ['#ff0080', '#ff33cc', '#ff66ff', '#cc00ff', '#9933ff', '#ff1493', '#ff69b4'];
      const emojis = ['❤️', '💖', '💕', '💓', '💗', '💞', '💘', '✨', '🌟', '💫'];
      
      for (let i = 0; i < 15; i++) {
        setTimeout(() => {
          const heart = document.createElement('div');
          heart.className = 'floating-heart';
          heart.textContent = emojis[Math.floor(Math.random() * emojis.length)];
          heart.style.left = x + (Math.random() - 0.5) * 80 + 'px';
          heart.style.top = y + (Math.random() - 0.5) * 80 + 'px';
          heart.style.color = colors[Math.floor(Math.random() * colors.length)];
          heart.style.fontSize = (Math.random() * 10 + 16) + 'px';
          document.body.appendChild(heart);

          // Animación más intensa
          heart.animate([
            { transform: 'translate(0, 0) scale(0.5)', opacity: 1 },
            { transform: `translate(${Math.random() * 100 - 50}px, -${Math.random() * 100 + 50}px) scale(1.2)`, opacity: 0.8 },
            { transform: `translate(${Math.random() * 120 - 60}px, -${Math.random() * 150 + 80}px) scale(0)`, opacity: 0 }
          ], {
            duration: 2000 + Math.random() * 1000,
            easing: 'cubic-bezier(0.2, 0.8, 0.7, 1)'
          });

          setTimeout(() => heart.remove(), 3000);
        }, i * 50);
      }
    }

    // Detectar clic/touch
    document.body.addEventListener('click', function(e) {
      if (e.target !== document.querySelector('.menu-btn') && !document.querySelector('.menu').contains(e.target)) {
        createTouchEffect(e.clientX, e.clientY);
      }
    });

    document.body.addEventListener('touchstart', function(e) {
      for (let touch of e.touches) {
        createTouchEffect(touch.clientX, touch.clientY);
      }
    });
  </script>

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

      const message = `En cada latido, pleno en ti.
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
