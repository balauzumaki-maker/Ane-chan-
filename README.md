<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Birthday Surprise</title>
    <style>
        body { display: flex; justify-content: center; align-items: center; height: 100vh; margin: 0; background-color: #ffe6f2; font-family: sans-serif; text-align: center; overflow: hidden; }
        #game-container, #surprise-container { padding: 30px; background: white; border-radius: 20px; box-shadow: 0 10px 25px rgba(0,0,0,0.1); width: 80%; }
        #surprise-container { display: none; }
        h1 { color: #ff4d94; font-size: 24px; }
        .buttons { margin-top: 40px; position: relative; height: 150px; }
        button { padding: 15px 35px; font-size: 18px; border: none; border-radius: 50px; cursor: pointer; transition: 0.2s; font-weight: bold; }
        #yes-btn { background-color: #ff4d94; color: white; position: absolute; left: 10%; }
        #no-btn { background-color: #f0f0f0; color: #666; position: absolute; right: 10%; }
        .birthday-text { font-size: 28px; color: #ff1a75; font-weight: bold; line-height: 1.5; }
        .cake { font-size: 50px; margin-top: 20px; }
    </style>
</head>
<body>

    <div id="game-container">
        <h1>Do you like me? 🥺</h1>
        <div class="buttons">
            <button id="yes-btn">Yes</button>
            <button id="no-btn">No</button>
        </div>
    </div>

    <div id="surprise-container">
        <div class="birthday-text">
            HAPPY BIRTHDAY <br> 
            ANE-CHAN 🤗🥰
        </div>
        <div class="cake">🎂🎉💖</div>
        <p style="color: #ff4d94; margin-top: 15px;">Have a wonderful day!<br>Unoda Life-la ellame nallatha nadakkum! <br> 
        Have a great year ahead! 🎂✨<br>
         I'm the best gift you'll ever get, so no more presents for you today! 🤗</p>
    </div>

    <script>
        const yesBtn = document.getElementById('yes-btn');
        const gameContainer = document.getElementById('game-container');
        const surpriseContainer = document.getElementById('surprise-container');
        let moveCount = 0;

        yesBtn.addEventListener('click', () => {
            if (moveCount < 5) {
                const x = Math.random() * (window.innerWidth - 120);
                const y = Math.random() * (window.innerHeight - 60);
                yesBtn.style.position = 'fixed';
                yesBtn.style.left = x + 'px';
                yesBtn.style.top = y + 'px';
                moveCount++;
            } else {
                gameContainer.style.display = 'none';
                surpriseContainer.style.display = 'block';
                document.body.style.backgroundColor = '#ffccf2';
            }
        });

        document.getElementById('no-btn').addEventListener('click', () => {
            alert("No-vaa😡? yes click pannu dii 😡");
        });
    </script>
</body>
</html>
