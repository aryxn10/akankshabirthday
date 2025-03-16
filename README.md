<!DOCTYPE html>
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
            background-image: url('AK2.jpg');
           background-size: cover; /* Makes image cover entire background */
        background-position: center; /* Centers the image */
background-repeat: no-repeat; /* Prevents image from repeating */
background-attachment: fixed; /* Image stays in place when scrolling */
        }
        
        .container {
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
            background-color: rgba(255, 255, 255, 0.8);
            border-radius: 15px;
            box-shadow: 0 8px 32px rgba(31, 38, 135, 0.37);
            backdrop-filter: blur(4px);
            margin-top: 20px;
            margin-bottom: 20px;
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
            border-radius: 10px;
        }
        
        .gift-box:before {
            content: '';
            position: absolute;
            width: 30px;
            height: 150px;
            background-color: #f50057;
            left: 50%;
            transform: translateX(-50%);
            border-radius: 5px;
            z-index: 1;
        }
        
        .gift-box:after {
            content: '';
            position: absolute;
            width: 150px;
            height: 30px;
            background-color: #f50057;
            top: 50%;
            transform: translateY(-50%);
            border-radius: 5px;
            z-index: 1;
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
        
        .photo-gallery {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 10px;
            margin: 20px 0;
        }
        
        .photo-frame {
            width: 150px;
            height: 150px;
            border: 5px solid white;
            box-shadow: 0 4px 8px rgba(0,0,0,0.2);
            overflow: hidden;
            border-radius: 10px;
            transition: transform 0.3s;
            cursor: pointer;
        }
        
        .photo-frame:hover {
            transform: scale(1.1);
        }
        
        .photo-frame img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        .memory-container {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0,0,0,0.8);
            z-index: 100;
            display: flex;
            justify-content: center;
            align-items: center;
            opacity: 0;
            transition: opacity 0.3s;
            pointer-events: none;
        }
        
        .memory-container.active {
            opacity: 1;
            pointer-events: all;
        }
        
        .memory {
            background-color: white;
            padding: 20px;
            border-radius: 10px;
            max-width: 600px;
            width: 80%;
            position: relative;
        }
        
        .close-memory {
            position: absolute;
            top: 10px;
            right: 10px;
            background: none;
            border: none;
            font-size: 20px;
            cursor: pointer;
            color: #e91e63;
        }
        
        .memory-title {
            font-size: 1.5rem;
            color: #e91e63;
            margin-bottom: 10px;
        }
        
        .memory-text {
            font-size: 1rem;
            color: #333;
        }
        
        .cake-container {
            position: relative;
            width: 200px;
            height: 200px;
            margin: 0 auto;
        }
        
        .cake-img {
            width: 100%;
            cursor: pointer;
        }
        
        .candle {
            position: absolute;
            top: 30px;
            width: 20px;
            height: 40px;
            background: linear-gradient(to bottom, #ffeb3b, #ffc107);
            border-radius: 10px 10px 0 0;
            z-index: 2;
        }
        
        .flame {
            position: absolute;
            top: -20px;
            left: 5px;
            width: 10px;
            height: 20px;
            background: linear-gradient(to bottom, #ff5722, #ff9800);
            border-radius: 50% 50% 20% 20%;
            animation: flicker 1s infinite alternate;
        }
        
        #countdown {
            font-size: 2rem;
            color: #e91e63;
            margin: 20px 0;
            font-weight: bold;
        }
        
        .birthday-wish {
            max-width: 400px;
            height: 100px;
            margin: 20px auto;
            padding: 10px;
            font-size: 1rem;
            border: 2px solid #e91e63;
            border-radius: 10px;
            resize: none;
        }
        
        .wishes-container {
            max-height: 200px;
            overflow-y: auto;
            margin: 20px 0;
            padding: 10px;
            background-color: rgba(255, 255, 255, 0.7);
            border-radius: 10px;
        }
        
        .wish {
            padding: 10px;
            margin: 10px 0;
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
            text-align: left;
        }
        
        .polaroid {
            background: white;
            padding: 10px 10px 30px 10px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
            transform: rotate(var(--rotation)); 
            transition: all 0.3s;
        }
        
        .polaroid:hover {
            transform: rotate(0deg) scale(1.05);
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
        
        @keyframes flicker {
            0%, 100% { transform: scaleY(1); }
            50% { transform: scaleY(1.2); }
        }
        
        .decoration {
            position: fixed;
            width: 100%;
            height: 50px;
            background-image: repeating-linear-gradient(45deg, #ff4081, #ff4081 10px, #f48fb1 10px, #f48fb1 20px);
            z-index: -1;
        }
        
        .decoration-top {
            top: 0;
        }
        
        .decoration-bottom {
            bottom: 0;
        }
    </style>
</head>
<body>
    <div class="decoration decoration-top"></div>
    <div class="decoration decoration-bottom"></div>
    <div class="balloons" id="balloons"></div>
    <div class="confetti-container" id="confetti"></div>
    
    <div class="container">
        <h1>Happy Birthday AKANKSHA!</h1>
        <div class="birthday-message">
            Wishing you an amazing day filled with joy, laughter, and wonderful memories!
        </div>
        
        <div id="countdown">Birthday Countdown: Loading...</div>
        
        <div class="cake-container">
            <img src="https://unsplash.com/photos/a-birthday-cake-with-lit-candles-sitting-on-a-table-GZ44SmEfMps" alt="Birthday Cake">
            <div class="candle" style="left: 90px;">
                <div class="flame" id="flame"></div>
            </div>
        </div>
        
        <div class="photo-gallery">
            <div class="photo-frame polaroid" style="--rotation: -5deg;" onclick="showMemory(1)">
                <img src="https://images.unsplash.com/photo-1527529482837-4698179dc6ce?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Birthday Memory">
            </div>
            <div class="photo-frame polaroid" style="--rotation: 3deg;" onclick="showMemory(2)">
                <img src="https://images.unsplash.com/photo-1530103862676-de8c9debad1d?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Birthday Memory">
            </div>
            <div class="photo-frame polaroid" style="--rotation: -2deg;" onclick="showMemory(3)">
                <img src="https://images.unsplash.com/photo-1464349153735-7db50ed83c84?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Birthday Memory">
            </div>
            <div class="photo-frame polaroid" style="--rotation: 4deg;" onclick="showMemory(4)">
                <img src="https://images.unsplash.com/photo-1523301343968-6a6ebf63c672?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Birthday Memory">
            </div>
        </div>
        
        <div class="gift-box" id="giftBox"></div>
        <div class="gift-message" id="giftMessage">
            Dear Akanksha, may your birthday be as beautiful and special as you are! 
            Here's to another amazing year of your life! 🎉
        </div>
        
        <button class="btn" id="playBtn">Play Birthday Song</button>
        <button class="btn" id="moreBtn">More Confetti!</button>
        <button class="btn" id="wishBtn">Make a Wish</button>
        
        <div id="wishingWell" style="display: none;">
            <textarea class="birthday-wish" id="wishText" placeholder="Write your birthday wish for Akanksha here..."></textarea>
            <button class="btn" id="submitWish">Submit Wish</button>
            
            <div class="wishes-container" id="wishesContainer">
                <div class="wish">
                    <strong>Mom & Dad:</strong> Happy birthday to our amazing daughter! We love you so much!
                </div>
                <div class="wish">
                    <strong>Best Friend:</strong> Cheers to another year of our crazy adventures! Happy birthday!
                </div>
            </div>
        </div>
    </div>
    
    <div class="memory-container" id="memoryContainer">
        <div class="memory">
            <button class="close-memory" onclick="closeMemory()">×</button>
            <h3 class="memory-title" id="memoryTitle">Memory Title</h3>
            <p class="memory-text" id="memoryText">Memory description goes here.</p>
            <img id="memoryImage" src="" alt="
<img id="memoryImage" src="" alt="Memory Image" style="max-width: 100%; margin-top: 15px; border-radius: 8px;">
        </div>
    </div>
    
    <audio id="birthdaySong" src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3"></audio>
    <audio id="blowSound" src="https://assets.mixkit.co/active_storage/sfx/212/212-preview.mp3"></audio>
    
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
        
        // Memory functions
        function showMemory(id) {
            const memories = [
                { title: "Birthday Celebrations", text: "Every year we celebrate with lots of fun and laughter!", image: "https://images.unsplash.com/photo-1527529482837-4698179dc6ce?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" },
                { title: "Special Moments", text: "Remember that time we had that amazing adventure? Memories we'll cherish forever!", image: "https://images.unsplash.com/photo-1530103862676-de8c9debad1d?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" },
                { title: "Friendship Goals", text: "Friends who celebrate together, stay together! Happy birthday, Akanksha!", image: "https://images.unsplash.com/photo-1464349153735-7db50ed83c84?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" },
                { title: "Happy Times", text: "Wishing you many more years of happiness and joy! May all your dreams come true.", image: "https://images.unsplash.com/photo-1523301343968-6a6ebf63c672?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" }
            ];
            
            const memory = memories[id-1];
            document.getElementById('memoryTitle').textContent = memory.title;
            document.getElementById('memoryText').textContent = memory.text;
            document.getElementById('memoryImage').src = memory.image;
            
            document.getElementById('memoryContainer').classList.add('active');
        }
        
        function closeMemory() {
            document.getElementById('memoryContainer').classList.remove('active');
        }
        
        // Birthday countdown
        function updateCountdown() {
            // Set to Akanksha's birthday - change this to the actual birthday
            const birthday = new Date("2025-03-17"); // Example date, replace with actual date
            const now = new Date();
            
            // For this year's birthday
            let thisYearBirthday = new Date(now.getFullYear(), birthday.getMonth(), birthday.getDate());
            
            // If this year's birthday has passed, calculate for next year
            if (now > thisYearBirthday) {
                thisYearBirthday = new Date(now.getFullYear() + 1, birthday.getMonth(), birthday.getDate());
            }
            
            const diff = thisYearBirthday - now;
            
            // Convert to days, hours, minutes, seconds
            const days = Math.floor(diff / (1000 * 60 * 60 * 24));
            const hours = Math.floor((diff % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            const minutes = Math.floor((diff % (1000 * 60 * 60)) / (1000 * 60));
            const seconds = Math.floor((diff % (1000 * 60)) / 1000);
            
            document.getElementById('countdown').innerHTML = `Birthday Countdown: ${days}d ${hours}h ${minutes}m ${seconds}s`;
            
            setTimeout(updateCountdown, 1000);
        }
        
        // Cake candle interaction
        function handleCakeClick() {
            const flame = document.getElementById('flame');
            const blowSound = document.getElementById('blowSound');
            
            if (flame.style.display !== 'none') {
                flame.style.display = 'none';
                blowSound.play();
                addMoreConfetti();
                
                setTimeout(() => {
                    alert("🎉 Happy Birthday, Akanksha! Your wish has been made! 🎉");
                }, 500);
                
                // Relight candle after some time
                setTimeout(() => {
                    flame.style.display = 'block';
                }, 10000);
            }
        }
        
        // Initialize the page
        window.onload = function() {
            createBalloons();
            createConfetti();
            updateCountdown();
            
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
            
            // Make a wish button
            const wishBtn = document.getElementById('wishBtn');
            const wishingWell = document.getElementById('wishingWell');
            
            wishBtn.addEventListener('click', function() {
                if (wishingWell.style.display === 'none') {
                    wishingWell.style.display = 'block';
                    wishBtn.textContent = "Hide Wishes";
                } else {
                    wishingWell.style.display = 'none';
                    wishBtn.textContent = "Make a Wish";
                }
            });
            
            // Submit wish
            const submitWish = document.getElementById('submitWish');
            const wishText = document.getElementById('wishText');
            const wishesContainer = document.getElementById('wishesContainer');
            
            submitWish.addEventListener('click', function() {
                if (wishText.value.trim() !== '') {
                    const newWish = document.createElement('div');
                    newWish.className = 'wish';
                    newWish.innerHTML = `<strong>Guest:</strong> ${wishText.value}`;
                    wishesContainer.prepend(newWish);
                    wishText.value = '';
                    
                    addMoreConfetti();
                }
            });
            
            // Blow candle interaction
            document.querySelector('.cake-img').addEventListener('click', handleCakeClick);
        };
    </script>
</body>
</html>
