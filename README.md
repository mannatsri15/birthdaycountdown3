# birthdaycountdown3
Happy 15 Soon Mahi!
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
            background-color: #ffcccb;
            color: #333;
        }
        h1 {
            margin-top: 20vh;
        }
        #countdown {
            font-size: 2em;
            font-weight: bold;
        }
    </style>
</head>
<body>
    <h1>Birthday Countdown 🎉</h1>
    <p id="countdown"></p>
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
    </script>
</body>
</html>

