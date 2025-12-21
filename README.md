<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>Master of Puppets</title>
    <style>
        * { box-sizing: border-box; }

        body {
            background-color: black;
            color: white;
            font-family: Arial, sans-serif;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            min-height: 100vh;
            margin: 0;
        }

        img {
            max-width: 100%;
            height: auto;
            object-fit: contain;
        }

        audio {
            width: 100%;
            max-width: 1024px;
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <div class="container">
        <img src="Master.png" alt="Master of Puppets" />
        <audio id="player" src="Metallica_-_Master_Of_Puppets.mp3" controls></audio>
    </div>

    <script>
        window.addEventListener('load', () => {
            setTimeout(() => {
                const player = document.getElementById('player');
                player.autoplay = true;
                player.play().catch(error => console.error('Воспроизведение заблокировано:', error));
            }, 100); // Небольшая задержка перед попыткой автозапуска
        });
    </script>
</body>
</html>
