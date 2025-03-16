
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Birthday Akanksha!</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            background-color: #fce4ec;
            font-family: 'Arial', sans-serif;
            overflow-x: hidden;
            text-align: center;
        }
        
        .container {
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
        }
        
        h1 {
            font-size: 3.5rem;
            color: #e91e63;
            margin-bottom: 10px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.2);
            animation: bounce 2s infinite;
        }
        
        .birthday-message {
            font-size: 1.5rem;
            color: #6a1b9a;
            margin-bottom: 30px;
        }
        
        .cake {
            font-size: 100px;
            margin: 20px 0;
            animation: rotate 10s infinite linear;
            display: inline-block;
        }
        
        .balloons {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: -1;
        }
        
        .balloon {
            position: absolute;
            width: 40px;
            height: 50px;
            border-radius: 50%;
            animation: float 15s infinite ease-in-out;
        }
        
        .confetti-container {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: -1;
        }
        
        .confetti {
            position: absolute;
            width: 10px;
            height: 10px;
            animation: fall 8s infinite linear;
        }
        
        .btn {
            background-color: #e91e63;
            color: white;
            border: none;
            padding: 12px 24px;
            font-size: 1.2rem;
            border-radius: 50px;
            cursor: pointer;
            margin: 10px;
            transition: all 0.3s;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        }
        
        .btn:hover {
            background-color: #c2185b;
            transform: scale(1.05);
        }
        
        .gift-box {
            width: 150px;
            height: 150px;
            background-color: #ff4081;
            position: relative;
            margin: 30px auto;
            animation: pulse 2s infinite;
            cursor: pointer;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
        }
        
        .gift-box:before {
            content: '';
            position: absolute;
            width: 30px;
            height: 150px;
            background-color: #f50057;
            left: 50%;
            transform: translateX(-50%);
        }
        
        .gift-box:after {
            content: '';
            position: absolute;
            width: 150px;
            height: 30px;
            background-color: #f50057;
            top: 50%;
            transform: translateY(-50%);
        }
        
        .gift-message {
            display: none;
            font-size: 1.5rem;
            color: #e91e63;
            margin: 20px 0;
            padding: 15px;
            background-color: rgba(255, 255, 255, 0.8);
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }
        
        @keyframes bounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-20px); }
        }
        
        @keyframes rotate {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }
        
        @keyframes float {
            0% { transform: translateY(100vh); opacity: 1; }
            100% { transform: translateY(-100px); opacity: 0; }
        }
        
        @keyframes fall {
            0% { transform: translateY(-100px) rotate(0deg); opacity: 1; }
            100% { transform: translateY(100vh) rotate(720deg); opacity: 0; }
        }
        
        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.05); }
        }
    </style>
</head>
<body>
    <div class="balloons" id="balloons"></div>
    <div class="confetti-container" id="confetti"></div>
    
    <div class="container">
        <h1>Happy Birthday AKANKSHA!</h1>
        <div class="birthday-message">
            Wishing you an amazing day filled with joy, laughter, and wonderful memories!
        </div>
        
        <div class="cake">🎂</div>
        
        <div class="gift-box" id="giftBox"></div>
        <div class="gift-message" id="giftMessage">
            Dear Akanksha, may your birthday be as beautiful and special as you are! 
            Here's to another amazing year of your life! 🎉
        </div>
        
        <button class="btn" id="playBtn">Play Birthday Song</button>
        <button class="btn" id="moreBtn">More Confetti!</button>
    </div>
    
    <audio id="birthdaySong" src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3"></audio>
    
    <script>
        // Create balloon elements
        function createBalloons() {
            const colors = ['#e91e63', '#9c27b0', '#3f51b5', '#2196f3', '#ff9800'];
            const balloonsContainer = document.getElementById('balloons');
            
            for (let i = 0; i < 30; i++) {
                const balloon = document.createElement('div');
                balloon.className = 'balloon';
                balloon.style.backgroundColor = colors[Math.floor(Math.random() * colors.length)];
                balloon.style.left = `${Math.random() * 100}%`;
                balloon.style.animationDuration = `${15 + Math.random() * 10}s`;
                balloon.style.animationDelay = `${Math.random() * 5}s`;
                balloonsContainer.appendChild(balloon);
            }
        }
        
        // Create confetti elements
        function createConfetti() {
            const colors = ['#e91e63', '#9c27b0', '#3f51b5', '#2196f3', '#ff9800', '#4caf50', '#8bc34a'];
            const confettiContainer = document.getElementById('confetti');
            
            for (let i = 0; i < 100; i++) {
                const confetti = document.createElement('div');
                confetti.className = 'confetti';
                confetti.style.backgroundColor = colors[Math.floor(Math.random() * colors.length)];
                confetti.style.left = `${Math.random() * 100}%`;
                confetti.style.width = `${5 + Math.random() * 10}px`;
                confetti.style.height = `${5 + Math.random() * 10}px`;
                confetti.style.opacity = Math.random();
                confetti.style.animationDuration = `${5 + Math.random() * 10}s`;
                confetti.style.animationDelay = `${Math.random() * 5}s`;
                confettiContainer.appendChild(confetti);
            }
        }
        
        // Add more confetti
        function addMoreConfetti() {
            const colors = ['#e91e63', '#9c27b0', '#3f51b5', '#2196f3', '#ff9800', '#4caf50', '#8bc34a'];
            const confettiContainer = document.getElementById('confetti');
            
            for (let i = 0; i < 50; i++) {
                const confetti = document.createElement('div');
                confetti.className = 'confetti';
                confetti.style.backgroundColor = colors[Math.floor(Math.random() * colors.length)];
                confetti.style.left = `${Math.random() * 100}%`;
                confetti.style.width = `${5 + Math.random() * 10}px`;
                confetti.style.height = `${5 + Math.random() * 10}px`;
                confetti.style.opacity = Math.random();
                confetti.style.animationDuration = `${5 + Math.random() * 10}s`;
                confetti.style.animationDelay = `0s`;
                confettiContainer.appendChild(confetti);
            }
        }
        
        // Initialize the page
        window.onload = function() {
            createBalloons();
            createConfetti();
            
            // Play button functionality
            const playBtn = document.getElementById('playBtn');
            const birthdaySong = document.getElementById('birthdaySong');
            
            playBtn.addEventListener('click', function() {
                if (birthdaySong.paused) {
                    birthdaySong.play();
                    playBtn.textContent = "Pause Birthday Song";
                } else {
                    birthdaySong.pause();
                    playBtn.textContent = "Play Birthday Song";
                }
            });
            
            // More confetti button
            const moreBtn = document.getElementById('moreBtn');
            moreBtn.addEventListener('click', addMoreConfetti);
            
            // Gift box click event
            const giftBox = document.getElementById('giftBox');
            const giftMessage = document.getElementById('giftMessage');
            
            giftBox.addEventListener('click', function() {
                if (giftMessage.style.display === 'block') {
                    giftMessage.style.display = 'none';
                } else {
                    giftMessage.style.display = 'block';
                    addMoreConfetti();
                }
            });
        };
    </script>
</body>
</html>
