<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gửi anh ngày 6/4</title>
    <link href="https://fonts.googleapis.com/css2?family=Pacifico&display=swap" rel="stylesheet">
    <style>
        body {
            background: linear-gradient(135deg, #ffecd2, #fcb69f);
            font-family: 'Pacifico', cursive;
            text-align: center;
            color: #ff4d6d;
            padding: 50px;
            animation: backgroundChange 5s infinite alternate;
        }

        @keyframes backgroundChange {
            0% {background: linear-gradient(135deg, #ffecd2, #fcb69f);}
            100% {background: linear-gradient(135deg, #ffe6fa, #c9f0ff);}
        }

        h1 {
            font-size: 3em;
            margin-bottom: 20px;
        }

        p {
            font-size: 1.8em;
        }

        .heart {
            position: fixed;
            width: 20px;
            height: 20px;
            background: pink;
            transform: rotate(45deg);
            top: -20px;
            animation: fall 5s linear infinite;
        }

        .heart::before,
        .heart::after {
            content: "";
            position: absolute;
            width: 20px;
            height: 20px;
            background: pink;
            border-radius: 50%;
        }

        .heart::before {
            top: -10px;
            left: 0;
        }

        .heart::after {
            left: -10px;
            top: 0;
        }

        @keyframes fall {
            to {
                transform: translateY(100vh) rotate(360deg);
            }
        }
    </style>
</head>
<body>
    <h1>Chúc anh 6/4 vui vẻ! 💖</h1>
    <p>Em chúc anh luôn mạnh khỏe, làm việc thật thuận lợi và lúc nào cũng vui tươi như nụ cười của anh! 😄</p>

    <audio autoplay loop>
        <source src="https://dl.dropboxusercontent.com/s/4iyb13kwy2j7g3u/Bruno%20Mars%20-%20Uptown%20Funk%20ft.%20Mark%20Ronson%20%28Official%20Audio%29.mp3" type="audio/mp3">
        Trình duyệt của bạn không hỗ trợ phát nhạc.
    </audio>

    <script>
        function createHeart() {
            const heart = document.createElement('div');
            heart.className = 'heart';
            heart.style.left = Math.random() * 100 + 'vw';
            heart.style.animationDuration = (Math.random() * 3 + 2) + 's';
            document.body.appendChild(heart);

            setTimeout(() => heart.remove(), 5000);
        }

        setInterval(createHeart, 300);
    </script>
</body>
</html>
