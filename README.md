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
            background-size: cover;
            background-position: center;
            background-repeat: no-repeat;
            background-attachment: fixed;
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
            z-index: 0;
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
            z-index: 0;
        }
        .confetti {
            position: absolute;
            width: 10px;
            height: 10px;
            animation: fall 8s infinite linear; 
            background-color: #f06292; /* Set a color */
            box-shadow: 0 0 5px rgba(0,0,0,0.3);
            border-radius: 50%; /* Makes circular confetti */
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
    transform: rotate(var(--rotation, 0deg)); /* Add this line */
}
        .candle {
    position: absolute;
    width: 10px;
    height: 30px;
    background-color: #ff9800;
    z-index: 2;
    border-radius: 5px;
}
.flame {
    position: absolute;
    width: 15px;
    height: 25px;
    background-color: #ff5722;
    border-radius: 50% 50% 50% 50% / 60% 60% 40% 40%;
    top: -20px;
    left: -2.5px;
    animation: flicker 0.5s infinite alternate;
    box-shadow: 0 0 10px 5px rgba(255, 87, 34, 0.7);
}
@keyframes flicker {
    0% { transform: scale(1); opacity: 1; }
    100% { transform: scale(0.9); opacity: 0.8; }
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
        .cake-container {
            position: relative;
            max-width: 200px;
            margin: 0 auto 20px;
        }
        .cake-container img {
            width: 100%;
            border-radius: 10px;
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
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0,0,0,0.8);
            z-index: 100; 
            justify-content: center;
            align-items: center;
            opacity: 0;
            transition: opacity 0.3s;
            pointer-events: none;
        }
        @keyframes rotate {
    0% { transform: rotate(0deg); }
    100% { transform: rotate(360deg); }
}
        .memory-container.active {
            opacity: 1;
            pointer-events: all;
        }
        .memory {
            background-color: white;
            padding: 20px;
            border-radius: 10px;
            max-width: min(600px, 80%);
            width: 100%;
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
        @keyframes bounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-20px); }
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
       <div class="confetti-container" id="confettiContainer"></div>
    <div class="container">
        <h1>HAPPY BIRTHDAY AKANKSHA!🎉🎂💖</h1>
        <div class="birthday-message">
            Wishing you a day filled with joy, laughter, and everything you love and a year ahead that's even better than the last.
        </div>
        

        <div class="cake-container">
            <img src="cake.jpg" alt="Birthday Cake">
            <div class="candle" style="left: 90px;">
                <div class="flame" id="flame"></div>
            </div>
        </div>

        <div class="photo-gallery">
            <div class="photo-frame" style="--rotation: -5deg;" onclick="showMemory(1)">
                <img src="AK4.jpg" alt="Birthday Memory">
            </div>
            <div class="photo-frame" style="--rotation: 3deg;" onclick="showMemory(2)">
                <img src="AK5.jpg">
            </div>
            <div class="photo-frame" style="--rotation: -2deg;" onclick="showMemory(3)">
                <img src="AK3.jpg">
                <div class="balloons" id="balloons"></div>
            </div>
            <div class="photo-frame" style="--rotation: 4deg;" onclick="showMemory(4)">
                <img src="AK1.jpg" alt="Birthday Memory">
            </div>
        </div>

        <div class="gift-box" id="giftBox"></div>
        <div class="gift-message" id="giftMessage">
            Dear Akanksha, On this special day, I just want to remind you how incredibly amazing you are. 
            You bring so much joy, love, and light into my life, and I’m beyond grateful for you every single day.
            May this year bring you endless happiness, success, and all the beautiful moments you deserve.
            Here’s to more laughter, adventures, and unforgettable memories together! 🥂✨
        </div>

        <button class="btn" id="playBtn">Play Birthday Song</button>
        <button class="btn" id="moreBtn">More Confetti!</button>
        <button class="btn" id="wishBtn">Make a Wish</button>

        <div id="wishingWell" style="display: none;">
            <textarea class="birthday-wish" id="wishText" placeholder="Write your birthday wish for Akanksha here..."></textarea>
            <button class="btn" id="submitWish">Submit Wish</button>

            <div class="wishes-container" id="wishesContainer"></div>
        </div>
    </div>

    <div class="memory-container" id="memoryContainer">
        <div class="memory">
            <button class="close-memory" onclick="closeMemory()">×</button>
            <h3 class="memory-title" id="memoryTitle">Memory Title</h3>
            <p class="memory-text" id="memoryText">Memory description goes here.</p>
            <img id="memoryImage" src="" alt="Memory Image" style="max-width: 100%; margin-top: 15px; border-radius: 8px;">
        </div>
    </div>
    
    <audio id="birthdaySong" src="birthday-song.mp3.mp3"></audio>
    <audio id="blowSound" src="https://assets.mixkit.co/active_storage/sfx/212/212-preview.mp3"></audio>

    <script>
        // Memory Viewer
        function showMemory(memoryId) {
            const memoryContainer = document.getElementById('memoryContainer');
            const memoryTitle = document.getElementById('memoryTitle');
            const memoryText = document.getElementById('memoryText');
            const memoryImage = document.getElementById('memoryImage');
            let title, text, imageSrc;

            if (memoryId === 1) {
                title = "BIRTHDAY TOGETHER";
                text = "17.03.2024";
                imageSrc = "AK4.jpg";
            } else if (memoryId === 2) {
                title = "SPECIAL MOMENTS";
                text = "Remember that time we had that amazing time? Memories we'll cherish forever!";
                imageSrc = "AK5.jpg";
            } else if (memoryId === 3) {
                title = "KEEP SMILING";
                text = "Have a wonderful day! Remember to smile, even when things get tough. You're amazing.";
                imageSrc = "AK3.jpg";
            } else {
                title = "LAST TIME TOGETHER";
                text = "I was just looking at the pictures from our last meet and it brought back such great memories.";
                imageSrc = "AK1.jpg";
            }
            // Add flame blow functionality
            document.getElementById('flame').addEventListener('click', function() {
    const blowSound = document.getElementById('blowSound');
    blowSound.play();
    this.style.opacity = 0;
    setTimeout(() => {
        this.style.opacity = 1;
    }, 3000);
    });
            memoryTitle.textContent = title;
            memoryText.textContent = text;
            memoryImage.src = imageSrc;

            memoryContainer.classList.add('active');
        }

        function closeMemory() {
            document.getElementById('memoryContainer').classList.remove('active');
        } 
        // Play Birthday Song
        document.getElementById('playBtn').addEventListener('click', function() {
        const song = document.getElementById('birthdaySong');
        
        // Add error handling
    song.onerror = function() {
        alert("Sorry, there was an error playing the birthday song.");
    };
    
    // Try to play the song
    song.play()
        .then(() => console.log("Birthday song playing"))
        .catch(error => {
            console.error("Error playing song:", error);
            alert("Could not play the birthday song. Please try again or check if audio is enabled.");
        });
});
        
        // Flame blow effect
        document.getElementById('flame').addEventListener('click', function() {
    const blowSound = document.getElementById('blowSound');
    blowSound.play();
    this.style.opacity = 0;
    setTimeout(() => {
        this.style.opacity = 1;
    }, 3000);
    }); 
    
    // More Confetti
    document.getElementById('moreBtn').addEventListener('click', function() {
    const confettiContainer = document.getElementById('confettiContainer');
    
    // Generate multiple confetti pieces
    for(let i = 0; i < 50; i++) {
        const confetti = document.createElement('div');
        confetti.classList.add('confetti');
        
        // Random position
        confetti.style.left = Math.random() * 100 + '%';
        
        // Random animation duration
        confetti.style.animationDuration = (Math.random() * 3 + 5) + 's';
        
        // Random colors
        const colors = ['#e91e63', '#9c27b0', '#3f51b5', '#2196f3', '#ff9800', '#ffeb3b'];
        const randomColor = colors[Math.floor(Math.random() * colors.length)];
        confetti.style.backgroundColor = randomColor;
        
        // Random size
        const size = Math.random() * 8 + 5;
        confetti.style.width = size + 'px';
        confetti.style.height = size + 'px';
        
        // Random rotation
        confetti.style.transform = `rotate(${Math.random() * 360}deg)`;
        
        confettiContainer.appendChild(confetti);
        
        // Remove confetti after animation completes
        setTimeout(() => {
            confetti.remove();
        }, 8000);
    }
    });
        // Make a Wish Button
        document.getElementById('wishBtn').addEventListener('click', function() {
            const wishingWell = document.getElementById('wishingWell');
            wishingWell.style.display = wishingWell.style.display === 'none' ? 'block' : 'none';
        });

        // Submit Wish
        document.getElementById('submitWish').addEventListener('click', function() {
            const wishText = document.getElementById('wishText').value;
            if (wishText) {
                const wishesContainer = document.getElementById('wishesContainer');
                const wish = document.createElement('div');
                wish.classList.add('wish');
                wish.textContent = wishText;
                wishesContainer.appendChild(wish);
                document.getElementById('wishText').value = '';
            }
        });

        // Gift Box Animation
        const giftBox = document.getElementById('giftBox');
        giftBox.addEventListener('click', function() {
            document.getElementById('giftMessage').style.display = 'block';
        });
    </script>
</body>
</html>
