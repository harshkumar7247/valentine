<Avantika>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>For You, My Love 💖</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
@import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@500;700&display=swap');

body {
  margin: 0;
  height: 100vh;
  overflow: hidden;
  font-family: 'Playfair Display', serif;
  background:
    radial-gradient(circle at top, rgba(255,182,193,0.5), rgba(0,0,0,0.7)),
    url("https://images.unsplash.com/photo-1509042239860-f550ce710b93");
  background-size: cover;
  background-position: center;
  display: flex;
  justify-content: center;
  align-items: center;
  color: white;
}

/* Romantic glow */
body::after {
  content: "";
  position: absolute;
  inset: 0;
  background: radial-gradient(circle, rgba(255,105,180,0.25), transparent 70%);
  z-index: 0;
}

/* Royal card */
.card {
  position: relative;
  z-index: 5;
  background: linear-gradient(135deg, rgba(255,255,255,0.35), rgba(255,255,255,0.08));
  backdrop-filter: blur(18px);
  padding: 65px 48px;
  border-radius: 36px;
  text-align: center;
  max-width: 520px;
  width: 90%;
  box-shadow: 0 40px 100px rgba(0,0,0,0.75);
  border: 2px solid rgba(255,215,200,0.9);
}

h1 {
  font-size: 2.8rem;
  margin-bottom: 35px;
  color: #fff0f8;
  text-shadow: 0 0 20px rgba(255,182,193,1);
}

p {
  font-size: 1.35rem;
  line-height: 1.7;
  margin-bottom: 35px;
  color: #fff3fa;
}

.buttons {
  display: flex;
  justify-content: center;
  gap: 36px;
}

button {
  padding: 18px 48px;
  font-size: 1.25rem;
  border-radius: 50px;
  border: none;
  cursor: pointer;
  font-family: 'Playfair Display', serif;
  transition: 0.4s;
}

.yes {
  background: linear-gradient(45deg, #ff7ab6, #ff2f7a);
  color: white;
  box-shadow: 0 0 25px rgba(255,105,180,1);
}

.yes:hover {
  transform: scale(1.18);
}

.no {
  background: #f2f2f2;
  color: #444;
}

.message {
  display: none;
  font-size: 1.9rem;
  line-height: 1.7;
  color: #fff3fa;
  text-shadow: 0 0 20px rgba(255,182,193,1);
}

/* Falling petals */
.petal {
  position: absolute;
  top: -10%;
  width: 40px;
  height: 40px;
  background-image: url("https://pngimg.com/uploads/petals/petals_PNG12.png");
  background-size: cover;
  opacity: 0.85;
  animation: fall linear infinite;
  z-index: 1;
}

@keyframes fall {
  to { transform: translateY(120vh) rotate(360deg); }
}

/* Sparkles */
.sparkle {
  position: absolute;
  width: 6px;
  height: 6px;
  background: radial-gradient(circle, #ffd700, transparent);
  border-radius: 50%;
  animation: sparkle 3s infinite;
  z-index: 2;
}

@keyframes sparkle {
  0% { opacity: 0; transform: scale(0); }
  50% { opacity: 1; transform: scale(1.6); }
  100% { opacity: 0; transform: scale(0); }
}

/* Hearts */
.heart {
  position: absolute;
  color: rgba(255,182,193,0.55);
  font-size: 22px;
  animation: floatUp 10s linear infinite;
  z-index: 2;
}

@keyframes floatUp {
  from { transform: translateY(100vh); opacity: 0; }
  to { transform: translateY(-10vh); opacity: 1; }
}
</style>
</head>

<body>

<script>
for (let i = 0; i < 30; i++) {
  let petal = document.createElement("div");
  petal.className = "petal";
  petal.style.left = Math.random() * 100 + "vw";
  petal.style.animationDuration = 6 + Math.random() * 6 + "s";
  document.body.appendChild(petal);
}

for (let i = 0; i < 45; i++) {
  let sparkle = document.createElement("div");
  sparkle.className = "sparkle";
  sparkle.style.left = Math.random() * 100 + "vw";
  sparkle.style.top = Math.random() * 100 + "vh";
  sparkle.style.animationDelay = Math.random() * 3 + "s";
  document.body.appendChild(sparkle);
}

for (let i = 0; i < 18; i++) {
  let heart = document.createElement("div");
  heart.className = "heart";
  heart.innerHTML = "❤";
  heart.style.left = Math.random() * 100 + "vw";
  heart.style.animationDuration = 8 + Math.random() * 6 + "s";
  document.body.appendChild(heart);
}
</script>

<div class="card">
  <h1 id="question">Will you be my Valentine? 💖</h1>

  <p id="text">
    Every moment with you feels like poetry,<br>
    every smile of yours feels like magic.<br><br>
    This Valentine’s Day, I just want one thing…
  </p>

  <div class="buttons" id="buttons">
    <button class="yes" onclick="yesClicked()">Yes 🌸</button>
    <button class="no">No</button>
  </div>

  <div class="message" id="message">
    Hey beautiful 💕<br>
    Thank you for choosing my heart.<br>
    Be my Valentine, my love —<br>
    let’s go on a date on <b>14 February</b> 🌹
  </div>
</div>

<script>
function yesClicked() {
  document.getElementById("question").style.display = "none";
  document.getElementById("text").style.display = "none";
  document.getElementById("buttons").style.display = "none";
  document.getElementById("message").style.display = "block";
}
</script>

</body>
</html>
