<html lang="en">
<head>
<meta charset="UTF-8">
<title>For Avantika ❤️</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
@import url('https://fonts.googleapis.com/css2?family=Great+Vibes&family=Playfair+Display:wght@500;700&display=swap');

body {
  margin: 0;
  height: 100vh;
  overflow: hidden;
  font-family: 'Playfair Display', serif;
  background:
    radial-gradient(circle at top, rgba(255,182,193,0.55), rgba(0,0,0,0.75)),
    url("https://images.unsplash.com/photo-1509042239860-f550ce710b93");
  background-size: cover;
  background-position: center;
  display: flex;
  justify-content: center;
  align-items: center;
  color: white;
}

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
  backdrop-filter: blur(20px);
  padding: 70px 50px;
  border-radius: 38px;
  text-align: center;
  max-width: 540px;
  width: 90%;
  box-shadow: 0 45px 110px rgba(0,0,0,0.8);
  border: 2px solid rgba(255,215,200,0.9);
}

/* Name */
.name {
  font-family: 'Great Vibes', cursive;
  font-size: 4rem;
  color: gold;
  margin-bottom: 10px;
  text-shadow: 0 0 25px rgba(255,215,0,1);
}

/* Question */
h1 {
  font-size: 2.6rem;
  margin: 20px 0 25px;
  color: #fff0f8;
  text-shadow: 0 0 22px rgba(255,182,193,1);
}

/* Text */
p {
  font-size: 1.35rem;
  line-height: 1.7;
  margin-bottom: 25px;
  color: #fff3fa;
}

/* Countdown */
#countdown {
  font-size: 1.25rem;
  margin-bottom: 35px;
  color: #ffd6e8;
  text-shadow: 0 0 12px rgba(255,182,193,1);
}

/* Buttons */
.buttons {
  display: flex;
  justify-content: center;
  gap: 40px;
}

button {
  padding: 18px 50px;
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
  box-shadow: 0 0 30px rgba(255,105,180,1);
}

.no {
  background: #f2f2f2;
  color: #444;
}

/* Heartbeat */
.heartbeat {
  animation: beat 1s infinite;
}

@keyframes beat {
  0%, 100% { transform: scale(1); }
  50% { transform: scale(1.15); }
}

/* Final message */
.message {
  display: none;
  font-size: 1.9rem;
  line-height: 1.7;
  color: #fff3fa;
  text-shadow: 0 0 22px rgba(255,182,193,1);
}

/* Petals */
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
</style>
</head>

<body>

<script>
/* Petals */
for (let i = 0; i < 28; i++) {
  let p = document.createElement("div");
  p.className = "petal";
  p.style.left = Math.random() * 100 + "vw";
  p.style.animationDuration = 6 + Math.random() * 6 + "s";
  document.body.appendChild(p);
}

/* Countdown */
const target = new Date("Feb 14, 2026 00:00:00").getTime();
setInterval(() => {
  const now = new Date().getTime();
  const diff = target - now;
  if (diff > 0) {
    const d = Math.floor(diff / (1000*60*60*24));
    const h = Math.floor((diff%(1000*60*60*24))/(1000*60*60));
    const m = Math.floor((diff%(1000*60*60))/(1000*60));
    document.getElementById("countdown").innerHTML =
      `Only <b>${d}</b> days <b>${h}</b> hrs <b>${m}</b> mins left for our day 💕`;
  }
}, 1000);
</script>

<div class="card">
  <div class="name">Avantika</div>

  <h1 id="question">Will you be my Valentine? ❤️</h1>

  <p id="text">
    You make ordinary moments feel special,<br>
    and my heart feels at home with you.
  </p>

  <div id="countdown">Counting the moments… 💕</div>

  <div class="buttons" id="buttons">
    <button class="yes" id="yesBtn" onclick="yesClicked()">Yes 💖</button>
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
  document.getElementById("yesBtn").classList.add("heartbeat");
  document.getElementById("question").style.display = "none";
  document.getElementById("text").style.display = "none";
  document.getElementById("buttons").style.display = "none";
  document.getElementById("message").style.display = "block";
}
</script>

</body>
</html>
