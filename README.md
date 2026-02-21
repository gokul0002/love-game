<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>For My Love ❤️</title>

<style>
    body {
        margin: 0;
        font-family: 'Comic Sans MS', cursive;
        background: linear-gradient(to right, #ff9a9e, #fad0c4);
        text-align: center;
        color: white;
        overflow-x: hidden;
    }

    h1 {
        margin-top: 20px;
        font-size: 3em;
        animation: glow 2s infinite alternate;
    }

    @keyframes glow {
        from { text-shadow: 0 0 10px white; }
        to { text-shadow: 0 0 20px red; }
    }

    .container {
        padding: 20px;
    }

    img {
        width: 200px;
        border-radius: 20px;
        margin: 10px;
    }

    button {
        padding: 12px 25px;
        margin: 10px;
        border: none;
        border-radius: 30px;
        font-size: 16px;
        cursor: pointer;
        transition: 0.3s;
    }

    .kiss {
        background-color: #ff4d6d;
        color: white;
    }

    .slap {
        background-color: #6c757d;
        color: white;
    }

    button:hover {
        transform: scale(1.1);
    }

    .game-box {
        margin-top: 30px;
        padding: 20px;
        background: rgba(255, 255, 255, 0.2);
        border-radius: 20px;
        display: inline-block;
    }

    #result {
        margin-top: 15px;
        font-size: 20px;
        font-weight: bold;
    }

    .heart {
        position: fixed;
        color: red;
        animation: float 5s linear infinite;
    }

    @keyframes float {
        from { transform: translateY(100vh); opacity: 1; }
        to { transform: translateY(-10vh); opacity: 0; }
    }
</style>
</head>

<body>

<h1>💖 For My Beautiful Girl 💖</h1>

<div class="container">

    <!-- Cute GIFs (Replace links with your favorite GIFs) -->
    <img src="https://media.giphy.com/media/3oriO0OEd9QIDdllqo/giphy.gif">
    <img src="https://media.giphy.com/media/l0HlBO7eyXzSZkJri/giphy.gif">
    <img src="https://media.giphy.com/media/26BRv0ThflsHCqDrG/giphy.gif">

    <h2>You are my sunshine 🌞</h2>
    <p>I love you more than words can ever say 💕</p>

    <!-- Game Section -->
    <div class="game-box">
        <h2>💋 Kiss Me or Slap Me Game 💔</h2>
        <p id="question">Click Start to Play!</p>
        <button onclick="nextQuestion()">Start Game</button>
        <br>
        <button class="kiss" onclick="answer('kiss')">💋 Kiss Me</button>
        <button class="slap" onclick="answer('slap')">😝 Slap Me</button>
        <p id="result"></p>
    </div>

</div>

<script>

const questions = [
    "If I forget our anniversary?",
    "If I eat your favorite chocolate?",
    "If I call you cute in front of friends?",
    "If I steal your fries?",
    "If I hug you randomly?"
];

let currentQuestion = -1;

function nextQuestion() {
    currentQuestion++;
    if (currentQuestion < questions.length) {
        document.getElementById("question").innerText = questions[currentQuestion];
        document.getElementById("result").innerText = "";
    } else {
        document.getElementById("question").innerText = "Game Over ❤️ I Still Love You!";
    }
}

function answer(choice) {
    let resultText = "";

    if (choice === "kiss") {
        resultText = "Aww 😘 I knew you love me!";
    } else {
        resultText = "Ouch 😝 I deserve that maybe!";
    }

    document.getElementById("result").innerText = resultText;

    setTimeout(nextQuestion, 1500);
}

// Floating hearts animation
setInterval(() => {
    let heart = document.createElement("div");
    heart.innerHTML = "❤️";
    heart.classList.add("heart");
    heart.style.left = Math.random() * 100 + "vw";
    heart.style.fontSize = Math.random() * 20 + 15 + "px";
    document.body.appendChild(heart);

    setTimeout(() => {
        heart.remove();
    }, 5000);
}, 500);

</script>

</body>
</html>
