# valentine-proposal
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>My Valentine 💖</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
body {
  margin: 0;
  height: 100vh;
  font-family: 'Georgia', serif;
  background:
    linear-gradient(rgba(0,0,0,0.45), rgba(0,0,0,0.45)),
    url("https://images.unsplash.com/photo-1501004318641-b39e6451bec6");
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  display: flex;
  justify-content: center;
  align-items: center;
  color: white;
}

.card {
  background: rgba(255,255,255,0.18);
  backdrop-filter: blur(10px);
  padding: 45px 35px;
  border-radius: 25px;
  text-align: center;
  box-shadow: 0 15px 40px rgba(0,0,0,0.5);
  max-width: 450px;
  width: 90%;
  border: 2px solid rgba(255,255,255,0.3);
}

h1 {
  font-size: 2.3rem;
  margin-bottom: 35px;
  color: #ffeef6;
  text-shadow: 2px 2px 10px rgba(0,0,0,0.6);
}

.buttons {
  display: flex;
  justify-content: center;
  gap: 25px;
}

button {
  padding: 14px 34px;
  font-size: 1.15rem;
  border-radius: 35px;
  border: none;
  cursor: pointer;
  transition: 0.3s;
}

.yes {
  background: linear-gradient(45deg, #ff4d88, #ff1a66);
  color: white;
}

.yes:hover {
  transform: scale(1.08);
}

.no {
  background: #e0e0e0;
  color: #444;
}

.message {
  display: none;
  font-size: 1.6rem;
  line-height: 1.6;
  color: #fff0f7;
  margin-top: 10px;
}
</style>
</head>

<body>

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

