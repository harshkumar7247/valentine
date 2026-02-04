<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>For Avantika ❤️</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<link href="https://fonts.googleapis.com/css2?family=Great+Vibes&family=Playfair+Display:wght@500;700&display=swap" rel="stylesheet">

<style>
body{
  margin:0;
  height:100vh;
  overflow:hidden;
  font-family:'Playfair Display',serif;
  background:
    radial-gradient(circle at top, rgba(255,182,193,0.5), rgba(0,0,0,0.85)),
    url("https://images.unsplash.com/photo-1526045612212-70caf35c14df");
  background-size:cover;
  background-position:center;
  display:flex;
  justify-content:center;
  align-items:center;
  color:white;
}

/* Card */
.card{
  position:relative;
  z-index:5;
  text-align:center;
  padding:70px 50px;
  background:linear-gradient(135deg, rgba(255,255,255,0.35), rgba(255,255,255,0.1));
  backdrop-filter:blur(18px);
  border-radius:40px;
  border:2px solid rgba(255,215,0,0.8);
  box-shadow:0 40px 100px rgba(0,0,0,0.8);
  max-width:600px;
  width:90%;
}

/* Name */
.name{
  font-family:'Great Vibes',cursive;
  font-size:4.5rem;
  color:gold;
  text-shadow:0 0 30px rgba(255,215,0,1);
}

/* Question */
h1{
  font-size:2.6rem;
  margin:20px 0;
  text-shadow:0 0 25px rgba(255,182,193,1);
}

/* Countdown */
#countdown{
  font-size:1.3rem;
  margin:25px 0 45px;
  color:#ffd6ea;
}

/* Floating YES */
.yes{
  position:fixed;
  bottom:18%;
  left:50%;
  transform:translateX(-50%);
  padding:18px 65px;
  font-size:1.4rem;
  border:none;
  border-radius:60px;
  background:linear-gradient(45deg,#ff7ab6,#ff2f7a);
  color:white;
  cursor:pointer;
  box-shadow:0 0 35px rgba(255,105,180,1);
  animation:floatBtn 3s ease-in-out infinite;
  z-index:10;
}

@keyframes floatBtn{
  0%,100%{ transform:translate(-50%,0); }
  50%{ transform:translate(-50%,-15px); }
}

/* Heartbeat */
.heartbeat{
  animation:beat 0.9s infinite;
}
@keyframes beat{
  0%,100%{ transform:translateX(-50%) scale(1); }
  50%{ transform:translateX(-50%) scale(1.15); }
}

/* Message */
.message{
  display:none;
  font-size:2.1rem;
  line-height:1.7;
  text-shadow:0 0 30px rgba(255,182,193,1);
}

/* Floating A hearts */
.heart{
  position:absolute;
  width:24px;
  height:24px;
  background:rgba(255,105,180,0.7);
  transform:rotate(45deg);
  animation:floatUp linear infinite;
}

.heart::before,
.heart::after{
  content:"";
  position:absolute;
  width:24px;
  height:24px;
  background:rgba(255,105,180,0.7);
  border-radius:50%;
}
.heart::before{ top:-12px; left:0; }
.heart::after{ left:-12px; top:0; }

.heart span{
  position:absolute;
  top:4px;
  left:7px;
  transform:rotate(-45deg);
  font-size:13px;
  font-weight:bold;
  color:white;
}

@keyframes floatUp{
  from{ transform:translateY(100vh) rotate(45deg); opacity:0; }
  to{ transform:translateY(-10vh) rotate(45deg); opacity:1; }
}
</style>
</head>

<body>

<!-- 🎵 Romantic Song -->
<audio id="bgMusic" loop>
  <!-- ADD YOUR MP3 FILE NAME HERE -->
  <source src="rakh-lo-tum-chhupa-ke.mp3" type="audio/mpeg">
</audio>

<script>
/* Floating hearts */
for(let i=0;i<30;i++){
  let h=document.createElement("div");
  h.className="heart";
  h.style.left=Math.random()*100+"vw";
  h.style.animationDuration=8+Math.random()*6+"s";
  h.innerHTML="<span>A</span>";
  document.body.appendChild(h);
}

/* Countdown */
const target=new Date("Feb 14, 2026 00:00:00").getTime();
setInterval(()=>{
  let now=new Date().getTime();
  let diff=target-now;
  if(diff>0){
    let d=Math.floor(diff/(1000*60*60*24));
    let h=Math.floor((diff%(1000*60*60*24))/(1000*60*60));
    let m=Math.floor((diff%(1000*60*60))/(1000*60));
    document.getElementById("countdown").innerHTML=
      `Only <b>${d}</b> days <b>${h}</b> hrs <b>${m}</b> mins left for us 💕`;
  }
},1000);

function yesClicked(){
  document.getElementById("bgMusic").play();
  document.getElementById("yesBtn").classList.add("heartbeat");
  document.getElementById("content").style.display="none";
  document.getElementById("message").style.display="block";
}
</script>

<div class="card">
  <div id="content">
    <div class="name">Avantika</div>
    <h1>Will you be my Valentine? ❤️</h1>
    <div id="countdown">Counting every heartbeat…</div>
  </div>

  <div class="message" id="message">
    Hey beautiful 💕<br>
    Thank you for choosing my heart.<br>
    Be my Valentine, my love —<br>
    let’s go on a date on <b>14 February</b> 🌹
  </div>
</div>

<button class="yes" id="yesBtn" onclick="yesClicked()">Yes 💖</button>

</body>
</html>
