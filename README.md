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
      background: linear-gradient(
          rgba(0,0,0,0.4),
          rgba(0,0,0,0.4)
        ),
        url("https://images.unsplash.com/photo-1526045612212-70caf35c14df");
      background-size: cover;
      background-position: center;
      display: flex;
      align-items: center;
      justify-content: center;
      color: #fff;
      text-align: center;
    }

    .card {
      background: rgba(255, 255, 255, 0.15);
      backdrop-filter: blur(8px);
      padding: 40px;
      border-radius: 20px;
      max-width: 420px;
      width: 90%;
      box-shadow: 0 10px 30px rgba(0,0,0,0.4);
    }

    h1 {
      font-size: 2.2rem;
      margin-bottom: 30px;
      color: #ffe6f2;
    }

    .buttons {
      display: flex;
      justify-content: center;
      gap: 20px;
      margin-top: 20px;
    }

    button {
      padding: 12px 28px;
      font-size: 1.1rem;
      border: none;
      border-radius: 30px;
      cursor: pointer;
      transition: 0.3s;
    }

    .yes {
      background: #ff4d88;
      color: white;
    }

    .yes:hover {
      background: #ff1a66;
    }

    .no {
      background: #cccccc;
      color: #333;
    }

    .message {
      display: none;
      font-size: 1.6rem;
      margin-top: 20px;
      color: #fff0f6;
    }
  </style>
</head>

<body>
  <div class="card">
    <h1 id="question">Will you be my Valentine? 💖</h1>

    <div class="buttons" id="buttons">
      <button class="yes" onclick="sayYes()">Yes 🌹</button>
      <button class="no">No</button>
    </div>

    <div class="message" id="message">
      Hey beautiful 💕<br>
      Thanks for being my Valentine, my love.<br>
      Let’s go on 14 Feb 🌸
    </div>
  </div>

  <script>
    function sayYes() {
      document.getElementById("question").style.display = "none";
      document.getElementById("buttons").style.display = "none";
      document.getElementById("message").style.display = "block";
    }
  </script>
</body>
</html>
