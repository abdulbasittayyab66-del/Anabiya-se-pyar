<!DOCTYPE html>
<html lang="hi">.
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Anabiya ke liye ❤️</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', sans-serif;
            background: linear-gradient(135deg, #ff9a9e 0%, #fecfef 50%, #fecfef 100%);
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: hidden;
            position: relative;
        }

        .love-letter {
            background: linear-gradient(135deg, #ff6b9d, #c44569);
            color: white;
            padding: 40px;
            border-radius: 25px;
            text-align: center;
            box-shadow: 0 25px 50px rgba(0,0,0,0.3);
            cursor: pointer;
            animation: letterFloat 3s ease-in-out infinite;
            max-width: 400px;
        }

        @keyframes letterFloat {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
        }

        .letter-text { font-size: 1.5em; margin-bottom: 20px; }
        .open-btn {
            background: #fff; color: #e91e63; border: none;
            padding: 15px 35px; border-radius: 25px;
            font-weight: bold; font-size: 1.1em;
            cursor: pointer; transition: all 0.3s ease;
        }
        .open-btn:hover { transform: scale(1.05); box-shadow: 0 10px 25px rgba(0,0,0,0.2); }

        .container {
            text-align: center;
            background: rgba(255,255,255,0.95);
            padding: 50px;
            border-radius: 25px;
            box-shadow: 0 25px 50px rgba(0,0,0,0.2);
            max-width: 500px;
            animation: fadeIn 1s ease;
            display: none;
            position: relative;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(30px); }
            to { opacity: 1; transform: translateY(0); }
        }

        h1 {
            font-size: 3em; color: #e91e63;
            margin-bottom: 15px;
        }

        .name-display {
            font-size: 2em; color: #ff4081;
            margin: 20px 0; font-weight: bold;
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.05); }
        }

        .buttons {
            display: flex; gap: 25px;
            justify-content: center; margin: 60px 0 20px 0;
        }

        button {
            padding: 15px 30px; font-size: 1.1em;
            border: none; border-radius: 30px;
            cursor: pointer; font-weight: bold;
            transition: all 0.3s ease;
        }

        .yes-btn {
            background: linear-gradient(45deg, #4CAF50, #45a049);
            color: white; box-shadow: 0 8px 20px rgba(76,175,80,0.4);
        }

        .yes-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 12px 25px rgba(76,175,80,0.6);
        }

        /* ULTRA FAST NO BUTTON - 0.25s SPEED */
        .no-btn {
            background: linear-gradient(45deg, #f44336, #da190b);
            color: white; box-shadow: 0 8px 20px rgba(244,67,54,0.4);
            padding: 10px 20px;
            font-size: 1em;
            position: relative;
            z-index: 100;
        }

        .no-btn.moving {
            position: absolute !important;
            transition: all 0.25s cubic-bezier(0.68, -0.55, 0.265, 1.55);
            transform: none !important;
        }

        .success-message {
            display: none; animation: bounceIn 1s ease-out;
        }

        @keyframes bounceIn {
            0% { transform: scale(0.3); opacity: 0; }
            50% { transform: scale(1.1); }
            100% { transform: scale(1); opacity: 1; }
        }

        .success-message.show { display: block; }

        .final-text {
            font-size: 1.8em; color: #4CAF50;
            margin: 20px 0; font-weight: bold;
            position: relative;
        }

        /* FLOWERS FOR CONGRATS */
        .flowers {
            position: fixed;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 200;
            display: none;
        }

        .flower {
            position: absolute;
            font-size: 25px;
            animation: flowerFloat 4s ease-out forwards;
        }

        @keyframes flowerFloat {
            0% {
                transform: translateY(100vh) scale(0) rotate(0deg);
                opacity: 1;
            }
            50% {
                transform: translateY(50vh) scale(1) rotate(180deg);
                opacity: 1;
            }
            100% {
                transform: translateY(-50px) scale(0.5) rotate(720deg);
                opacity: 0;
            }
        }

        .note {
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: white; padding: 25px;
            border-radius: 15px; margin: 30px 0;
            font-size: 1em; line-height: 1.6;
            opacity: 0; transform: translateY(20px);
            transition: all 0.8s ease;
        }

        .note.show {
            opacity: 1; transform: translateY(0);
        }

        .creator {
            font-size: 0.9em; color: #ff4081;
            margin-top: 20px; font-style: italic;
        }

        @media (max-width: 480px) {
            .container { padding: 30px 20px; }
            h1 { font-size: 2.2em; }
            .buttons { flex-direction: column; gap: 15px; margin: 40px 0 15px 0; }
        }
    </style>
</head>
<body>
    <div class="love-letter" onclick="openMain()">
        <div class="letter-text">
            💌 Anabiya ke liye 💌<br>
            Click to Open!
        </div>
        <button class="open-btn">OPEN 💕</button>
    </div>

    <!-- FLOWERS CONTAINER -->
    <div class="flowers" id="flowers"></div>
    
    <div class="container" id="mainContainer">
        <h1>❤️ Anabiya ❤️</h1>
        <div class="name-display">Anabiya Jee!</div>
        
        <div class="note" id="note">
            <strong>📝 Note:</strong><br>
            Anabiya jee/artist jee, ye website mene apke liye banai hai. Ik relationship me nhi ana chhati thi lekin ab to aa jao! Ab to apki 10th class bhi complete ho gai hai. Main bhi tumse pyar karta hun, lekin agar aise hi bol deta to normal lagta, isliye mene ye special website banai hai apke liye. Haan karne se pehle ek baar No wale button par zaroor click karna - meri mehnat lagi hai! 😊
        </div>

        <div class="buttons">
            <button class="no-btn" id="noBtn">No 😢</button>
            <button class="yes-btn" id="yesBtn">Yes 💕</button>
        </div>

        <div class="success-message" id="successMsg">
            <div class="final-text">🎉 Congratulations! Ab chat pe aao meri cutie pie! 💕</div>
        </div>

        <div class="creator">
            Made by Abdul Basit 💖 your crush
        </div>
    </div>

    <script>
        let noClicks = 0;
        // 10 ULTRA FAST POSITIONS
        let noBtnPositions = [
            {top: '10%', left: '5%'},
            {top: '10%', right: '5%'},
            {top: '25%', left: '8%'},
            {top: '25%', right: '8%'},
            {top: '40%', left: '12%'},
            {top: '40%', right: '12%'},
            {top: '60%', left: '6%'},
            {top: '60%', right: '6%'},
            {top: '75%', left: '10%'},
            {top: '75%', right: '10%'}
        ];

        function openMain() {
            document.querySelector('.love-letter').style.display = 'none';
            document.getElementById('mainContainer').style.display = 'block';
            setTimeout(() => {
                document.getElementById('note').classList.add('show');
            }, 500);
        }

        // ULTRA FAST NO BUTTON - 0.25s SPEED
        document.getElementById('noBtn').addEventListener('click', function(e) {
            e.preventDefault();
            noClicks++;
            
            const container = document.getElementById('mainContainer');
            const noBtn = this;
            
            // Random position from 10 positions
            const randomPos = noBtnPositions[Math.floor(Math.random() * noBtnPositions.length)];
            
            noBtn.classList.add('moving');
            noBtn.style.position = 'absolute';
            noBtn.style.zIndex = '1000';
            
            if (randomPos.left) {
                noBtn.style.left = randomPos.left;
                noBtn.style.right = 'auto';
            } else {
                noBtn.style.right = randomPos.right;
                noBtn.style.left = 'auto';
            }
            noBtn.style.top = randomPos.top;
            
            // ULTRA FAST 0.25s transition
            setTimeout(() => {
                noBtn.classList.remove('moving');
            }, 250);
            
            if (noClicks >= 5) {
                alert('😂 No button har jagah bhag gaya! Ab Yes kar do please! 💕');
            }
        });

        function showSuccess() {
            document.getElementById('successMsg').classList.add('show');
            document.querySelector('.buttons').style.display = 'none';
            document.getElementById('note').style.display = 'none';
            
            // FLOWERS URAO CONGRATS PE
            createFlowers();
        }

        // FLOWERS FUNCTION
        function createFlowers() {
            const flowersContainer = document.getElementById('flowers');
            flowersContainer.style.display = 'block';
            
            const flowers = ['🌸','🌺','🌹','🌷','💐','🌻','🌼','🪷'];
            
            for (let i = 0; i < 30; i++) {
                setTimeout(() => {
                    const flower = document.createElement('div');
                    flower.className = 'flower';
                    flower.innerHTML = flowers[Math.floor(Math.random() * flowers.length)];
                    flower.style.left = Math.random() * 100 + '%';
                    flower.style.animationDuration = (Math.random() * 2 + 3) + 's';
                    flowersContainer.appendChild(flower);
                    
                    setTimeout(() => flower.remove(), 5000);
                }, i * 100);
            }
        }

        // Yes button onclick
        document.getElementById('yesBtn').onclick = showSuccess;
    </script>
</body>
</html>
