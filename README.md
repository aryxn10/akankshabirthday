<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Birthday!</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            background: linear-gradient(135deg, #ff9a9e 0%, #fad0c4 100%);
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            color: #333;
        }
        .container {
            background-color: rgba(255, 255, 255, 0.9);
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
            padding: 40px;
            max-width: 600px;
            text-align: center;
            animation: fadeIn 1.5s ease-in-out;
        }
        h1 {
            color: #ff5e7d;
            margin-bottom: 20px;
            font-size: 2.5rem;
        }
        .name {
            font-size: 3rem;
            font-weight: bold;
            color: #ff3366;
            margin: 20px 0;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.1);
        }
        .message {
            font-size: 1.2rem;
            line-height: 1.6;
            margin-bottom: 30px;
        }
        .photo-frame {
            width: 300px;
            height: 300px;
            margin: 0 auto 30px;
            border-radius: 50%;
            overflow: hidden;
            border: 8px solid white;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }
        .photo {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        .hearts {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: -1;
        }
        .heart {
            position: absolute;
            width: 20px;
            height: 20px;
            background-color: #ff5e7d;
            transform: rotate(45deg);
            opacity: 0;
            animation: float 10s ease-in infinite;
        }
        .heart:before,
        .heart:after {
            content: '';
            width: 20px;
            height: 20px;
            background-color: #ff5e7d;
            border-radius: 50%;
            position: absolute;
        }
        .heart:before {
            top: -10px;
            left: 0;
        }
        .heart:after {
            top: 0;
            left: -10px;
        }
        button {
            background-color: #ff3366;
            color: white;
            border: none;
            padding: 12px 24px;
            font-size: 1.2rem;
            border-radius: 30px;
            cursor: pointer;
            transition: transform 0.3s, background-color 0.3s;
            margin-top: 20px;
            font-weight: bold;
        }
        button:hover {
            background-color: #ff1a53;
            transform: translateY(-3px);
        }
        @keyframes float {
            0% {
                transform: rotate(45deg) translateY(0px);
                opacity: 0;
            }
            10% {
                opacity: 1;
            }
            90% {
                opacity: 0;
            }
            100% {
                transform: rotate(45deg) translateY(-1000px);
                opacity: 0;
            }
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(30px); }
            to { opacity: 1; transform: translateY(0); }
        }
    </style>
</head>
<body>
    <div class="hearts" id="hearts"></div>
    <div class="container">
        <h1>Happy Birthday!</h1>
        <div class="name" id="AKANKSHA">Name</div>
        <div class="photo-frame">
            <img src="/api/placeholder/400/400" alt="AKANKSHA" class="photo" id="girlfriendPhoto">
        </div>
        <div class="message">
            On your special day, I want to celebrate you and all the joy you bring to my life. 
            Your smile lights up my world, and I'm so grateful for every moment we share together.
            Wishing you a day filled with happiness, laughter, and unforgettable memories.
            <br><br>
            With all my love,
        </div>
        <button id="surpriseBtn">Click For A Surprise!</button>
    </div>

    <script>
        // Function to create falling hearts animation
        function createHearts() {
            const heartsContainer = document.getElementById('hearts');
            const numberOfHearts = 20;
            
            for (let i = 0; i < numberOfHearts; i++) {
                const heart = document.createElement('div');
                heart.classList.add('heart');
                
                // Random position and delay
                const left = Math.random() * 100;
                const delay = Math.random() * 5;
                const size = Math.random() * 15 + 10;
                
                heart.style.left = left + 'vw';
                heart.style.animationDelay = delay + 's';
                heart.style.width = size + 'px';
                heart.style.height = size + 'px';
                
                heartsContainer.appendChild(heart);
            }
        }

        // Update the name function
        function updateName() {
            // Get the girlfriend's name from URL parameters
            const urlParams = new URLSearchParams(window.location.search);
            const name = urlParams.get('name');
            
            if (name) {
                document.getElementById('girlfriendName').textContent = name;
                document.title = Happy Birthday, ${name}!;
            }
        }

        // Surprise function
        function surprise() {
            const container = document.querySelector('.container');
            container.style.animation = 'pulse 0.5s ease-in-out';
            
            // Create more hearts
            createHearts();
            
            // Play birthday song (you could add music if you had it)
            alert('Happy Birthday to You! 🎂🎉');
        }

        // Initialize
        document.addEventListener('DOMContentLoaded', function() {
            createHearts();
            updateName();
            document.getElementById('surpriseBtn').addEventListener('click', surprise);
        });
    </script>
</body>
</html>
