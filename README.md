<!DOCTYPE html>
<html lang="de">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Date Anfrage 💖</title>

  <style>
    body {
      margin: 0;
      height: 100vh;
      overflow: hidden;
      display: flex;
      justify-content: center;
      align-items: center;
      background: linear-gradient(135deg, #ffdde1, #ee9ca7);
      font-family: Arial, sans-serif;
    }

    .container {
      text-align: center;
    }

    h1 {
      font-size: 2.5rem;
      color: white;
      margin-bottom: 40px;
    }

    button {
      padding: 15px 30px;
      font-size: 1.2rem;
      border: none;
      border-radius: 12px;
      cursor: pointer;
      position: absolute;
      transition: 0.15s;
    }

    #yesBtn {
      background-color: #4CAF50;
      color: white;
      left: 45%;
      top: 60%;
    }

    #noBtn {
      background-color: #ff4d4d;
      color: white;
      left: 55%;
      top: 60%;
    }

    .success {
      font-size: 3rem;
      color: white;
      animation: pop 0.5s ease;
    }

    @keyframes pop {
      0% { transform: scale(0.5); opacity: 0; }
      100% { transform: scale(1); opacity: 1; }
    }
  </style>
</head>
<body>

  <div class="container">
    <h1>Willst du mit mir auf ein Date gehen? 💕</h1>

    <button id="yesBtn">Ja ❤️</button>
    <button id="noBtn">Nein 💔</button>
  </div>

  <script>
    const noBtn = document.getElementById("noBtn");
    const yesBtn = document.getElementById("yesBtn");

    noBtn.addEventListener("mouseover", () => {
      const maxX = window.innerWidth - noBtn.offsetWidth;
      const maxY = window.innerHeight - noBtn.offsetHeight;

      const randomX = Math.random() * maxX;
      const randomY = Math.random() * maxY;

      noBtn.style.left = `${randomX}px`;
      noBtn.style.top = `${randomY}px`;
    });

    yesBtn.addEventListener("click", () => {
      document.body.innerHTML = `
        <div style="display:flex;justify-content:center;align-items:center;height:100vh;flex-direction:column;background:linear-gradient(135deg,#ff9a9e,#fad0c4);">
          <div class="success">
            Yaaay 💖<br>
            Date bestätigt 😍
          </div>
        </div>
      `;
    });
  </script>

</body>
</html>
