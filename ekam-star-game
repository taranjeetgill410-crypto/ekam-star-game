<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Catch the Stars, Ekam ⭐</title>

  <style>
    body {
      margin: 0;
      height: 100vh;
      overflow: hidden;
      background: linear-gradient(#87ceeb, #ffffff);
      font-family: "Comic Sans MS", cursive;
      text-align: center;
    }

    h1 {
      margin-top: 15px;
      font-size: 2.2rem;
      color: #ff9800;
    }

    #score {
      font-size: 1.6rem;
      color: #333;
    }

    .star {
      position: absolute;
      font-size: 50px;
      cursor: pointer;
      animation: pop 0.3s ease;
    }

    @keyframes pop {
      from { transform: scale(0); }
      to { transform: scale(1); }
    }

    .footer {
      position: fixed;
      bottom: 10px;
      width: 100%;
      font-size: 1.2rem;
      color: #555;
    }
  </style>
</head>

<body>

  <h1>Catch the Stars, Ekam ⭐</h1>
  <div id="score">Stars caught: 0</div>

  <div class="footer">Tap the ⭐ to collect them!</div>

  <audio id="ding">
    <source src="https://www.soundjay.com/buttons/sounds/button-3.mp3" type="audio/mpeg">
  </audio>

  <script>
    let score = 0;
    const scoreDisplay = document.getElementById("score");
    const sound = document.getElementById("ding");

    function createStar() {
      const star = document.createElement("div");
      star.className = "star";
      star.innerHTML = "⭐";

      star.style.left = Math.random() * (window.innerWidth - 60) + "px";
      star.style.top = Math.random() * (window.innerHeight - 120) + "px";

      star.onclick = () => {
        score++;
        scoreDisplay.innerHTML = "Stars caught: " + score;
        sound.play();
        star.remove();
      };

      document.body.appendChild(star);

      setTimeout(() => {
        if (star.parentNode) star.remove();
      }, 3000);
    }

    setInterval(createStar, 1200);
  </script>

</body>
</html>
