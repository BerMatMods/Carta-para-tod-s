<!DOCTYPE html><html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>BerMatModZ - Red Social Hack</title>
    <link href="https://fonts.googleapis.com/css2?family=Share+Tech+Mono&display=swap" rel="stylesheet">
    <style>
        body {
            background-color: #000;
            color: #0f0;
            font-family: 'Share Tech Mono', monospace;
            overflow: hidden;
            background-image: url('https://wallpapercave.com/wp/wp4043022.jpg');
            background-size: cover;
            background-blend-mode: overlay;
        }
        h1 {
            color: #f00;
            text-align: center;
            font-size: 3em;
            margin-top: 20px;
            text-shadow: 0 0 10px #f00;
        }
        .console {
            padding: 20px;
            background-color: rgba(0, 0, 0, 0.8);
            border-radius: 15px;
            margin: 20px auto;
            width: 90%;
            height: 500px;
            overflow-y: scroll;
            box-shadow: 0 0 15px #0f0, 0 0 30px #f00;
            backdrop-filter: blur(5px);
        }
        .line {
            margin: 5px 0;
            white-space: nowrap;
        }
        .typing {
            border-right: 2px solid #0f0;
            display: inline;
            animation: blink 0.7s steps(1) infinite;
        }
        @keyframes blink {
            0%, 100% { border-color: #0f0; }
            50% { border-color: transparent; }
        }
        .highlight {
            color: #f00;
            text-shadow: 0 0 5px #f00;
        }
        .alert-box {
            position: fixed;
            top: 20%;
            left: 50%;
            transform: translateX(-50%);
            background-color: #111;
            color: #0f0;
            padding: 20px;
            border-radius: 10px;
            text-align: center;
            box-shadow: 0 0 20px #f00;
            animation: popup 0.8s ease-in-out infinite alternate;
            border: 2px solid #f00;
            backdrop-filter: blur(5px);
        }
        @keyframes popup {
            0% { transform: translate(-50%, -10px); }
            100% { transform: translate(-50%, 10px); }
        }
    </style>
</head>
<body>
    <h1>⚡ BerMatModZ - Red Social Hack ⚡</h1>
    <div class="console" id="console"></div>
    <div class="alert-box" id="alert-box" style="display: none;">
        ⚠️ Tu teléfono ha sido inyectado con el antivirus de BerMatModZ ⚠️<br>
        📱 Protección total activada.<br>
        🔒 Disfruta de máxima seguridad mientras estés en nuestro servicio.
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
