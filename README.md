# kirti
hey babe
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>For Kirti ❤️</title>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Poppins', sans-serif;
}

body {
    background: radial-gradient(circle at top, #240046, #000);
    height: 100vh;
    overflow: hidden;
    display: flex;
    justify-content: center;
    align-items: center;
    color: white;
}

.container {
    text-align: center;
    max-width: 90%;
    animation: fadeIn 2s ease-in-out;
}

h1 {
    font-size: 2.6rem;
    margin-bottom: 20px;
    opacity: 0;
    animation: textAppear 2s forwards;
}

p {
    font-size: 1.4rem;
    opacity: 0;
    animation: textAppear 2s forwards;
    animation-delay: 2s;
}

.question {
    font-size: 3rem;
    margin-top: 40px;
    color: #ff4d6d;
    opacity: 0;
    animation: textAppear 2s forwards;
    animation-delay: 4s;
    cursor: pointer;
}

.yes {
    display: none;
    font-size: 2rem;
    margin-top: 30px;
    color: #ffd6e0;
    animation: pop 1s infinite alternate;
}

@keyframes fadeIn {
    from { opacity: 0; }
    to { opacity: 1; }
}

@keyframes textAppear {
    from {
        opacity: 0;
        transform: translateY(25px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

@keyframes pop {
    from { transform: scale(1); }
    to { transform: scale(1.12); }
}

/* Floating hearts */
.heart {
    position: absolute;
    color: #ff4d6d;
    font-size: 20px;
    animation: float 6s linear infinite;
}

@keyframes float {
    from {
        transform: translateY(100vh) scale(1);
        opacity: 1;
    }
    to {
        transform: translateY(-10vh) scale(1.6);
        opacity: 0;
    }
}
</style>
</head>

<body>

<!-- Romantic Music -->
<audio autoplay loop>
    <source src="https://cdn.pixabay.com/download/audio/2022/03/15/audio_aa8df7b0b5.mp3" type="audio/mp3">
</audio>

<div class="container">
    <h1>Hey Kirti Azad ❤️</h1>
    <p>
        Every moment with you feels special…<br>
        You make my ordinary days magical ✨
    </p>
    <div class="question" onclick="showYes()">
        Will you be my Valentine? 💖
    </div>
    <div class="yes" id="yesText">
        YAYYYY! You just made me the happiest ❤️🥹
    </div>
</div>

<script>
function createHeart() {
    const heart = document.createElement("div");
    heart.classList.add("heart");
    heart.innerHTML = "❤️";
    heart.style.left = Math.random() * 100 + "vw";
    heart.style.fontSize = Math.random() * 25 + 15 + "px";
    heart.style.animationDuration = Math.random() * 3 + 4 + "s";
    document.body.appendChild(heart);

    setTimeout(() => {
        heart.remove();
    }, 6000);
}

setInterval(createHeart, 300);

function showYes() {
    document.getElementById("yesText").style.display = "block";
}
</script>

</body>
</html>
