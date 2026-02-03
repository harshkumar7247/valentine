# valentine-proposal
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
  z-index: 2;
  background: linear-gradient(
    135deg,
    rgba(255,255,255,0.25),
    rgba(255,255,255,0.05)
  );
  backdrop-filter: blur(14px);
  padding: 55px 40px;
  border-radius: 30px;
  text-align: center;
  max-width: 460px;
  width: 90%;
  box-shadow: 0 25px 60px rgba(0,0,0,0.6);
  border: 2px solid rgba(255,215,230,0.6);
}

/* 👑 Heading */
h1 {
  font-size: 2.5rem;
  margin-bottom: 40px;
  color: #ffeaf4;
  text-shadow: 2px 2px 12px rgba(0,0,0,0.7);
}

/* 💕 Buttons */
.buttons {
  display: flex;
  justify-content: center;
  gap: 30px;
}

button {
  padding: 15px 38px;
  font-size: 1.15rem;
  border-radius: 40px;
  border: none;
  cursor: pointer;
  font-family: 'Playfair Display', serif;
  transition: 0.35s;
}

.yes {
  background: linear-gradient(45deg, #ff5fa2, #ff2f7a);
  color: white;
  box-shadow: 0 8px 25px rgba(255,47,122,0.6);
}

.yes:hover {
  transform: scale(1.1);
}

.no {
  background: #eeeeee;
  color: #444;
}

/* 💌 Message */
.message {
  display: none;
  font-size: 1.65rem;
  line-height: 1.6;
  color: #fff1f8;
}

/* 🌸 Falling Lily Petals */
.petal {
  position: absolute;
  top: -10%;
  width: 35px;
  height: 35px;
  background-image: url("https://pngimg.com/uploads/petals/petals_PNG12.png");
  background-size: cover;
  opacity: 0.8;
  animation: fall linear infinite;
}

@keyframes fall {
  0% {
    transform: translateY(0) rotate(0deg);
  }
  100% {
    transform: translateY(120vh) rotate(360deg);
  }
}
</style>
</head>

<body>

<!-- 🌸 Petals Container -->
<script>
for (let i = 0; i < 25; i++) {
  let petal = document.createElement("div");
  petal.className = "petal";
  petal.style.left = Math.random() * 100 + "vw";
  petal.style.animationDuration = 6 + Math.random() * 6 + "s";
  petal.style.opacity = Math.random();
  petal.style.transform = "scale(" + (0.5 + Math.random()) + ")";
  document.body.appendChild(petal);
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
