# valentine-proposal
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>My Valentine 💖</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
@import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@500;700&display=swap');

body {
  margin: 0;
  height: 100vh;
  overflow: hidden;
  font-family: 'Playfair Display', serif;
  background:
    linear-gradient(rgba(0,0,0,0.45), rgba(0,0,0,0.45)),
    url("https://images.unsplash.com/photo-1501004318641-b39e6451bec6");
  background-size: cover;
  background-position: center;
  display: flex;
  justify-content: center;
  align-items: center;
  color: white;
}

/* 🌸 Royal Glass Card */
.card {
  position: relative;
  z-index: 3;
  background: linear-gradient(
    135deg,
    rgba(255,255,255,0.28),
    rgba(255,255,255,0.06)
  );
  backdrop-filter: blur(16px);
  padding: 60px 45px;
  border-radius: 32px;
  text-align: center;
  max-width: 480px;
  width: 90%;
  box-shadow: 0 30px 80px rgba(0,0,0,0.65);
  border: 2px solid rgba(255,215,180,0.7);
}

/* 👑 Heading */
h1 {
  font-size: 2.6rem;
  margin-bottom: 42px;
  color: #fff0f8;
  text-shadow: 
    0 0 10px rgba(255,182,193,0.8),
    0 0 25px rgba(255,105,180,0.6);
}

/* 💕 Buttons */
.buttons {
  display: flex;
  justify-content: center;
  gap: 32px;
}

button {
  padding: 16px 42px;
  font-size: 1.2rem;
  border-radius: 45px;
  border: none;
  cursor: pointer;
  font-family: 'Playfair Display', serif;
  transition: 0.4s;
}

.yes {
  background: linear-gradient(45deg, #ff6aa2, #ff2f7a);
  color: white;
  box-shadow:
    0 0 15px rgba(255,105,180,0.8),
    0 0 35px rgba(255,20,147,0.6);
}

.yes:hover {
  transform: scale(1.12);
}

.no {
  background: #f1f1f1;
  color: #444;
}

/* 💌 Message */
.message {
  display: none;
  font-size: 1.75rem;
  line-height: 1.6;
  color: #fff2f9;
  text-shadow: 0 0 15px rgba(255,182,193,0.8);
}

/* 🌸 Falling Lily Petals */
.petal {
  position: absolute;
  top: -10%;
  width: 36px;
  height: 36px;
  background-image: url("https://pngimg.com/uploads/petals/petals_PNG12.png");
  background-size: cover;
  opacity: 0.8;
  animation: fall linear infinite;
  z-index: 1;
}

@keyframes fall {
  0% {
    transform: translateY(0) rotate(0deg);
  }
  100% {
    transform: translateY(120vh) rotate(360deg);
  }
}

/* ✨ Gold Sparkles */
.sparkle {
  position: absolute;
  width: 6px;
  height: 6px;
  background: radial-gradient(circle, #ffd700, transparent);
  border-radius: 50%;
  opacity: 0.8;
  animation: sparkle 3s infinite ease-in-out;
  z-index: 2;
}

@keyframes sparkle {
  0% {
    transform: scale(0);
    opacity: 0;
  }
  50% {
    transform: scale(1.5);
    opacity: 1;
  }
  100% {
    transform: scale(0);
    opacity: 0;
  }
}
</style>
</head>

<body>

<script>
/* 🌸 Lily Petals */
for (let i = 0; i < 28; i++) {
  let petal = document.createElement("div");
  petal.className = "petal";
  petal.style.left = Math.random() * 100 + "vw";
  petal.style.animationDuration = 6 + Math.random() * 6 + "s";
  petal.style.opacity = Math.random();
  petal.style.transform = "scale(" + (0.5 + Math.random()) + ")";
  document.body.appendChild(petal);
}

/* ✨ Gold Sparkles */
for (let i = 0; i < 40; i++) {
  let sparkle = document.createElement("div");
  sparkle.className = "sparkle";
  sparkle.style.left = Math.random() * 100 + "vw";
  sparkle.style.top = Math.random() * 100 + "vh";
  sparkle.style.animationDelay = Math.random() * 3 + "s";
  document.body.appendChild(sparkle);
}
</script>

<div class="card">
  <h1 id="question">Will you be my Valentine? 💖</h1>

  <div class="buttons" id="buttons">
    <button class="yes" onclick="yesClicked()">Yes 🌸</button>
    <button class="no">No</button>
  </div>

  <div class="message" id="message">
    Hey beautiful 💕<br>
    Thanks for being my Valentine, my love.<br>
    Let’s go on a date on <b>14 Feb</b> 🌹
  </div>
</div>

<script>
function yesClicked() {
  document.getElementById("question").style.display = "none";
  document.getElementById("buttons").style.display = "none";
  document.getElementById("message").style.display = "block";
}
</script>

</body>
</html>
