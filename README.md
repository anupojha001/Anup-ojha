<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Will You Be Mine?</title>
  <style>
    body {
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background: linear-gradient(to right, #ffdee9, #b5fffc);
      margin: 0;
      font-family: 'Arial', sans-serif;
    }
    .heart {
      width: 100px;
      height: 100px;
      background-color: red;
      position: relative;
      transform: rotate(-45deg);
      animation: pulse 1s infinite;
    }
    .heart:before,
    .heart:after {
      content: "";
      width: 100px;
      height: 100px;
      background-color: red;
      border-radius: 50%;
      position: absolute;
    }
    .heart:before { top: -50px; left: 0; }
    .heart:after { left: 50px; top: 0; }
    @keyframes pulse {
      0%, 100% { transform: rotate(-45deg) scale(1); }
      50% { transform: rotate(-45deg) scale(1.1); }
    }
    .message {
      position: absolute;
      top: 65%;
      text-align: center;
      font-size: 1.5rem;
      color: #333;
      max-width: 80%;
      animation: fadeIn 2s ease forwards;
      opacity: 0;
    }
    @keyframes fadeIn {
      to { opacity: 1; }
    }
    .button {
      margin-top: 20px;
      padding: 10px 20px;
      font-size: 1.2rem;
      background: #ff4b5c;
      color: white;
      border: none;
      border-radius: 25px;
      cursor: pointer;
      transition: background 0.3s ease;
    }
    .button:hover { background: #e43e51; }
  </style>
</head>
<body>

<audio autoplay loop>
  <source src="https://www.bensound.com/bensound-music/bensound-romantic.mp3" type="audio/mpeg">
  Your browser does not support the audio element.
</audio>

<div class="heart"></div>
<div class="message">
  From the moment I met you,<br>
  You filled my world with joy and love.<br>
  Every heartbeat whispers Anup Ojha.<br><br>
  <strong>Will you be mine forever?</strong><br>
  <button class="button" onclick="respond()">Yes!</button>
</div>

<script>
  function respond() {
    alert("Yay! You just made me the happiest person alive!");
  }
</script>

</body>
</html>
