<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Jump Scare Prank</title>
  <style>
    body {
      background-color: black;
      color: white;
      text-align: center;
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
    }
    #startScreen {
      margin-top: 100px;
    }
    #scareScreen {
      display: none;
      background-color: black;
      height: 100vh;
      width: 100vw;
      position: fixed;
      top: 0;
      left: 0;
      z-index: 9999;
    }
    #scareImage {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }
    #scareText {
      position: absolute;
      top: 20px;
      left: 50%;
      transform: translateX(-50%);
      font-size: 60px;
      color: red;
      text-shadow: 2px 2px 10px black;
    }
  </style>
</head>
<body>

<div id="startScreen">
  <h1>Click to start the fun!</h1>
  <button id="startButton" style="font-size: 24px; padding: 10px 20px;">Start</button>
</div>

<div id="scareScreen">
  <img id="scareImage" src="https://i.imgur.com/8km9sYb.jpg" alt="Scary Face">
  <div id="scareText">YOU'RE HACKED</div>
  <audio id="scareSound" src="https://www.soundjay.com/horror/sounds/scream-1.mp3"></audio>
</div>

<script>
  const startButton = document.getElementById('startButton');
  const startScreen = document.getElementById('startScreen');
  const scareScreen = document.getElementById('scareScreen');
  const scareSound = document.getElementById('scareSound');

  startButton.addEventListener('click', () => {
    startScreen.style.display = 'none';
    
    setTimeout(() => {
      scareScreen.style.display = 'block';
      scareSound.play();
    }, 2000); // 2-second delay before the scare
  });
</script>

</body>
</html>
