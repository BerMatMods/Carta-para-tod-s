<!DOCTYPE html><html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>BerMatModZ - Red Social Hack</title>
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@700&family=Roboto+Mono:wght@500&family=VT323&display=swap" rel="stylesheet">
    <style>
        body {
            background-color: #000000;
            color: #00ff00;
            font-family: 'VT323', monospace;
            overflow: hidden;
            background-image: radial-gradient(circle, #010101, #020202, #050505, #080808, #0b0b0b, #0f0f0f, #121212, #151515, #191919, #1c1c1c, #1f1f1f, #222222);
        }
        h1 {
            color: #ff0000;
            text-align: center;
            font-size: 4em;
            margin-top: 20px;
            text-shadow: 0 0 20px #ff0000, 0 0 40px #00ff00, 0 0 60px #0000ff;
            background: linear-gradient(90deg, #ff0000, #00ff00, #0000ff, #ff0000);
            -webkit-background-clip: text;
            color: transparent;
            animation: neon 2s infinite alternate;
        }
        @keyframes neon {
            0% { text-shadow: 0 0 30px #00ff00, 0 0 60px #ff0000, 0 0 90px #0000ff; }
            100% { text-shadow: 0 0 50px #ff0000, 0 0 80px #00ff00, 0 0 120px #0000ff; }
        }
        .console {
            padding: 20px;
            background-color: rgba(0, 0, 0, 0.9);
            border-radius: 15px;
            margin: 20px auto;
            width: 90%;
            height: 500px;
            overflow-y: scroll;
            box-shadow: 0 0 30px #00ff00, 0 0 60px #ff0000;
            border: 2px solid #00ff00;
        }
        .line {
            margin: 5px 0;
            white-space: nowrap;
        }
        .typing {
            border-right: 2px solid #00ff00;
            display: inline;
            animation: blink 0.7s steps(1) infinite;
        }
        @keyframes blink {
            0%, 100% { border-color: #00ff00; }
            50% { border-color: transparent; }
        }
        .alert-box {
            position: fixed;
            top: 20%;
            left: 50%;
            transform: translateX(-50%);
            background-color: #000000;
            color: #00ff00;
            padding: 20px;
            border-radius: 15px;
            text-align: center;
            box-shadow: 0 0 30px #ff0000, 0 0 60px #00ff00;
            border: 2px solid #ff0000;
            animation: popup 0.8s ease-in-out infinite alternate;
        }
        @keyframes popup {
            0% { transform: translate(-50%, -10px); }
            100% { transform: translate(-50%, 10px); }
        }
        a {
            color: #00ff00;
            text-decoration: none;
            font-family: 'Orbitron', sans-serif;
            font-weight: bold;
        }
        a:hover {
            color: #ff0000;
            text-shadow: 0 0 10px #ff0000, 0 0 20px #00ff00;
        }
    </style>
</head>
<body>
    <h1>⚡ BerMatModZ - Red Social Hack ⚡</h1>
    <div class="console" id="console"></div>
    <div class="alert-box" id="alert-box" style="display: none;">
        ⚠️ Tu teléfono ha sido inyectado con el antivirus de BerMatModZ ⚠️<br>
        📱 Protección total activada.<br>
        🔒 Disfruta de máxima seguridad mientras estés en nuestro servicio.<br>
        🌐 Contacto: <a href="https://github.com/Anthzberrocal" target="_blank">GitHub</a> | <a href="https://www.facebook.com/profile.php?id=100094869097190" target="_blank">Facebook</a> | <a href="https://wa.me/937556459" target="_blank">WhatsApp</a>
    </div>
    <script>
        const lines = [
            'Iniciando conexión segura con la red...',
            'Estableciendo túneles cifrados...',
            'Verificando identidad: BerMatModZ...',
            'Acceso autorizado ✅',
            'Recopilando información de la víctima...',
            'Cargando archivos del servidor...',
            'Comprometiendo cuentas de redes sociales...',
            'Inyectando códigos maliciosos en los servidores...',
            'Filtrando datos privados...',
            'Obteniendo mensajes privados...',
            'Accediendo a fotografías y videos...',
            'Simulando rastreo geográfico...',
            'Acceso total concedido...',
            '⚠️ Sistema comprometido: Todos los datos han sido clonados.',
            'El sistema ha sido comprometido por BerMatModZ, uno de los hackers más temidos del mundo, experto en ciberseguridad, inteligencia artificial y tecnología avanzada.',
            'Control total establecido. Sin rastros. 🕶️',
            'Sistema seguro cerrado.'
        ];const consoleElement = document.getElementById('console');
    let index = 0;

    function typeLine(line) {
        const div = document.createElement('div');
        div.className = 'line';
        consoleElement.appendChild(div);

        let charIndex = 0;
        function typeChar() {
            div.textContent += line[charIndex];
            charIndex++;
            if (charIndex < line.length) {
                setTimeout(typeChar, 50);
            }
        }
        typeChar();
    }

    function typeAllLines() {
        if (index < lines.length) {
            typeLine(lines[index]);
            index++;
            setTimeout(typeAllLines, 1000);
        } else {
            const done = document.createElement('div');
            done.className = 'line typing';
            done.textContent = 'Sistema seguro cerrado.';
            consoleElement.appendChild(done);
            showAlert();
        }
    }

    function showAlert() {
        const alertBox = document.getElementById('alert-box');
        alertBox.style.display = 'block';
        setTimeout(() => alertBox.style.display = 'none', 5000);
    }

    typeAllLines();
</script>

</body>
</html>
