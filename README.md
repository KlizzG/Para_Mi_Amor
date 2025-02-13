
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Para mi Amor, Aurora</title>
    <style>
        /* Estilos generales */
        body {
            margin: 0;
            padding: 0;
            font-family: 'Arial', sans-serif;
            background-color: #f9d9d7; /* Color de fondo suave */
            color: #5a3e36; /* Color de texto */
            text-align: center;
            display: flex;
            flex-direction: column;
            align-items: center;
            min-height: 100vh;
            overflow-y: auto; /* Habilita el scroll vertical */
        }

        h1 {
            font-size: 3rem;
            margin-bottom: 20px;
            color: #c44569; /* Color rosa oscuro */
            text-shadow: 0 0 5px #ff0077, 0 0 10px #ff0077, 0 0 20px #ff0077, 0 0 40px #ff0077;
            animation: neonGlow 1.5s infinite alternate;
        }

        @keyframes neonGlow {
            from { text-shadow: 0 0 5px #ff0077, 0 0 10px #ff0077, 0 0 20px #ff0077, 0 0 40px #ff0077; }
            to { text-shadow: 0 0 10px #ff0077, 0 0 20px #ff0077, 0 0 40px #ff0077, 0 0 80px #ff0077; }
        }

        p {
            font-size: 1.2rem;
            line-height: 1.6;
            max-width: 600px;
            margin: 0 auto 20px;
        }

        .container {
            background: rgba(255, 255, 255, 0.8); /* Fondo semi-transparente */
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
            margin: 20px;
            animation: fadeIn 2s ease-in-out;
            width: 90%; /* Ajusta el ancho para dispositivos móviles */
            max-width: 800px; /* Limita el ancho máximo */
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        /* Estilos del contador */
        #countdown {
            font-size: 2rem;
            font-weight: bold;
            color: #c44569;
            margin: 20px 0;
        }

        /* Estilos de la fecha de inicio */
        #start-date {
            font-size: 1.5rem;
            color: #5a3e36;
            margin-bottom: 10px;
        }

        /* Estilos de la galería */
        .gallery {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 10px;
            margin-top: 20px;
        }

        .gallery img {
            width: 150px;
            height: 150px;
            object-fit: cover;
            border-radius: 10px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease;
            animation: fadeIn 1.5s ease-in-out;
        }

        .gallery img:hover {
            transform: scale(1.1);
        }

        /* Estilos del corazón matemático */
        .math-heart {
            margin-top: 30px;
            font-size: 1.2rem;
            color: #5a3e36;
        }

        .math-heart canvas {
            border: 2px solid #c44569;
            border-radius: 10px;
            margin-top: 10px;
        }

        /* Estilos del corazón */
        .heart {
            color: #c44569;
            font-size: 2rem;
        }

        /* Botón de "Haz clic en mí" */
        button {
            padding: 10px 20px;
            background-color: #c44569;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            margin-top: 20px;
        }

        /* Mensajes ocultos */
        .hidden-message {
            display: none;
            font-size: 1rem;
            color: #5a3e36;
            margin-top: 10px;
        }

        .text-with-message {
            position: relative;
            cursor: pointer;
        }

        .text-with-message:hover .hidden-message {
            display: block;
        }
    </style>
</head>
<body>
    <!-- Reproductor de música -->
    <audio id="background-music" controls>
    <source src="cancion.mp3" type="audio/mpeg">
    Tu navegador no soporta la reproducción de audio.
</audio>

    <!-- Botón para reproducir música -->
    <button onclick="reproducirMusica()" style="position: fixed; top: 20px; right: 20px;">
        Reproducir música 🎵
    </button>

    <div class="container">
        <h1>Para mi Amor, Aurora <span class="heart">❤️</span></h1>
        <!-- Texto central -->
        <p>
            Querida Aurora, cada día a tu lado es un regalo. Eres mi razón para sonreír y mi inspiración para ser mejor. Te amo más de lo que las palabras pueden expresar.
        </p>
        <p>
            Hoy celebramos dos años de esta maravillosa historia que empezó hace mucho más tiempo, cuando nos conocimos en la universidad. Aunque en ese momento no sabía que el destino nos había preparado algo tan especial, siempre supe que había algo mágico en ti. En estos años juntos, me he dado cuenta de que el amor no es solo un sentimiento, sino una decisión constante de cuidarnos, entendernos y crecer juntos, y contigo a mi lado todo ha sido más fácil y hermoso.<br><br>
            No puedo dejar de sonreír al recordar todos los momentos que hemos compartido, las risas, las conversaciones profundas y hasta las pequeñas cosas que hacen que cada día valga la pena. Eres mi compañera, mi amiga, mi amor, y lo que más agradezco es saber que este viaje de vida lo compartimos juntos.<br><br>
            Hoy celebro no solo los dos años que hemos pasado como pareja, sino todos los años en los que nuestras vidas se cruzaron, como si el universo tuviera planeado todo para que hoy te pudiera decir con todo mi corazón que te amo más de lo que las palabras pueden expresar.<br><br>
            Te amo, Aurora. Gracias por ser tú, por darme tu amor, por ser mi refugio y mi razón para seguir adelante. Aquí estamos, celebrando este hermoso camino que hemos recorrido juntos, y sé que lo mejor está por venir.<br><br>
            Feliz aniversario, mi amor, te amo hoy y siempre.<br><br>
            Con todo mi amor,<br>
            Jiménez Garita José Luis
        </p>
        <!-- Fecha de inicio -->
        <div id="start-date">
            Nuestra relación comenzó el <strong>14 de febrero de 2023</strong>.
        </div>
        <!-- Contador -->
        <div id="countdown"></div>
        <!-- Botón de "Haz clic en mí" -->
        <button onclick="mostrarMensaje()">Haz clic en mí</button>
    </div>

    <!-- Galería de fotos -->
    <div class="container">
        <h2>Nuestros Momentos <span class="heart">❤️</span></h2>
        <div class="gallery">
            <img src="imagen1.jpg" alt="Foto 1">
            <div class="hidden-message">Este fue nuestro primer viaje juntos. 💖</div>
            <img src="imagen2j.jpg" alt="Foto 2">
            <div class="hidden-message">Aquí celebramos nuestro primer aniversario. 🎉</div>
            <img src="imagen3.jpg" alt="Foto 3">
            <div class="hidden-message">Este día fue mágico. ✨</div>
        </div>
    </div>

    <!-- Corazón matemático -->
    <div class="container math-heart">
        <h2>Un Corazón en R² <span class="heart">❤️</span></h2>
        <p>
            Este corazón está definido por la ecuación:<br>
            <strong>(x² + y² - 1)³ - x² · y³ = 0</strong>
        </p>
        <canvas id="heartCanvas" width="300" height="300"></canvas>
    </div>

    <!-- Script para el contador -->
    <script>
        // Fecha en que comenzaron a salir (14 de febrero de 2023)
        const startDate = new Date("2023-02-14").getTime();

        function updateCountdown() {
            const now = new Date().getTime();
            const timeDiff = now - startDate;

            // Calcula días, horas, minutos y segundos
            const days = Math.floor(timeDiff / (1000 * 60 * 60 * 24));
            const hours = Math.floor((timeDiff % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            const minutes = Math.floor((timeDiff % (1000 * 60 * 60)) / (1000 * 60));
            const seconds = Math.floor((timeDiff % (1000 * 60)) / 1000);

            // Muestra el contador
            document.getElementById("countdown").innerHTML = `
                Llevamos juntos:<br>
                ${days} días, ${hours} horas, ${minutes} minutos y ${seconds} segundos.
            `;
        }

        // Actualiza el contador cada segundo
        setInterval(updateCountdown, 1000);
        updateCountdown(); // Inicializa el contador
    </script>

    <!-- Script para dibujar el corazón -->
    <script>
        const canvas = document.getElementById("heartCanvas");
        const ctx = canvas.getContext("2d");

        // Escala y traslación para centrar el corazón
        const scale = 100;
        const offsetX = canvas.width / 2;
        const offsetY = canvas.height / 2;

        // Función para evaluar la ecuación del corazón
        function heartEquation(x, y) {
            return Math.pow(x * x + y * y - 1, 3) - x * x * Math.pow(y, 3);
        }

        // Dibuja el corazón
        function drawHeart() {
            ctx.clearRect(0, 0, canvas.width, canvas.height); // Limpia el canvas
            ctx.strokeStyle = "#c44569"; // Color del corazón
            ctx.lineWidth = 2;

            // Recorre los puntos del canvas
            for (let px = 0; px < canvas.width; px++) {
                for (let py = 0; py < canvas.height; py++) {
                    // Convierte coordenadas de píxeles a coordenadas matemáticas
                    const x = (px - offsetX) / scale;
                    const y = (offsetY - py) / scale;

                    // Evalúa la ecuación del corazón
                    if (Math.abs(heartEquation(x, y)) < 0.01) {
                        ctx.beginPath();
                        ctx.arc(px, py, 1, 0, 2 * Math.PI); // Dibuja un punto
                        ctx.stroke();
                    }
                }
            }
        }

        // Dibuja el corazón al cargar la página
        drawHeart();
    </script>

    <!-- Script para el botón de "Haz clic en mí" -->
    <script>
        function mostrarMensaje() {
            alert("¡Eres lo mejor que me ha pasado, Aurora! Cada día a tu lado es un regalo. Te amo infinitamente. ❤️");
        }
    </script>

    <!-- Script para reproducir música -->
    <script>
        function reproducirMusica() {
            const musica = document.getElementById("background-music");
            musica.play()
                .then(() => {
                    console.log("La música se está reproduciendo.");
                })
                .catch((error) => {
                    console.error("Error al reproducir la música:", error);
                    alert("No se pudo reproducir la música. Asegúrate de que el archivo esté en la carpeta correcta y en formato MP3.");
                });
        }
    </script>

    <!-- Script para mensajes ocultos en el texto -->
    <script>
        const textoCentral = document.querySelector("p");
        const mensajesOcultos = [
            "Eres mi razón para sonreír cada día. 💖",
            "Cada momento a tu lado es un tesoro. 🌟",
            "Eres mi inspiración para ser mejor. ✨",
            "Tu amor ilumina mi vida. 🌈",
        ];

        // Divide el texto en partes y agrega mensajes ocultos
        const partesTexto = textoCentral.innerHTML.split(".");
        textoCentral.innerHTML = partesTexto
            .map((parte, index) => {
                if (index < mensajesOcultos.length) {
                    return `<span class="text-with-message">${parte}.<div class="hidden-message">${mensajesOcultos[index]}</div></span>`;
                }
                return `${parte}.`;
            })
            .join(" ");
    </script>
</body>
</html>
