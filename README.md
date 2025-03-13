<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Birthday Countdown</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background: url('https://source.unsplash.com/1600x900/?birthday,celebration') no-repeat center center/cover;
            color: white;
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
        }
        .overlay {
            background: rgba(0, 0, 0, 0.5);
            padding: 20px;
            border-radius: 15px;
        }
        h1 {
            font-size: 2.5em;
            margin-bottom: 10px;
        }
        p {
            font-size: 1.5em;
        }
        #countdown {
            font-size: 2.5em;
            font-weight: bold;
            margin-top: 10px;
        }
    </style>
</head>
<body>
    <div class="overlay">
        <h1>Happy Birthday Countdown! 🎂🎉</h1>
        <p>Counting down to your special day...</p>
        <p id="countdown"></p>
    </div>
    <script>
        function updateCountdown() {
            const birthday = new Date('March 15, 2025 00:00:00').getTime();
            const now = new Date().getTime();
            const timeLeft = birthday - now;
            
            const days = Math.floor(timeLeft / (1000 * 60 * 60 * 24));
            const hours = Math.floor((timeLeft % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            const minutes = Math.floor((timeLeft % (1000 * 60 * 60)) / (1000 * 60));
            const seconds = Math.floor((timeLeft % (1000 * 60)) / 1000);
            
            document.getElementById("countdown").innerHTML = `${days}d ${hours}h ${minutes}m ${seconds}s left`;
        }
        setInterval(updateCountdown, 1000);
        updateCountdown();
    </script>
</body>
</html>
