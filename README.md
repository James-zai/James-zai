<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Happy Birthday</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <div class="card">
    <button id="openCard" class="button">Open Card</button>
    <div id="message" class="hidden">
      <h1>Happy Birthday, Jane!</h1>
      <p>You are the most special person in my life.</p>
      <p>Do you love me?</p>
      <button id="yesButton" class="button">Yes</button>
      <button id="noButton" class="button">No</button>
    </div>
  </div>
  <div id="animation" class="hidden">
    <div class="flowers"></div>
    <div class="lights"></div>
    <h1 class="love-message">I Love You, Jane</h1>
  </div>
  <script src="script.js"></script>
</body>
</html>

body {
  font-family: Arial, sans-serif;
  text-align: center;
  background-color: #fff0f5;
  margin: 0;
  padding: 20px;
}

.card {
  margin: 100px auto;
  padding: 20px;
  border: 2px solid pink;
  border-radius: 10px;
  background-color: #ffe4e1;
  width: 300px;
  box-shadow: 0 0 15px rgba(255, 105, 180, 0.5);
}

.button {
  padding: 10px 20px;
  background-color: pink;
  border: none;
  border-radius: 5px;
  color: white;
  cursor: pointer;
  font-size: 16px;
}

.button:hover {
  background-color: #ff69b4;
}

.hidden {
  display: none;
}

#animation {
  position: relative;
  width: 100%;
  height: 100vh;
  background-color: #ffebef;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}

.flowers {
  width: 100px;
  height: 100px;
  background: url('flower.png') no-repeat center;
  background-size: contain;
  animation: floatUp 3s ease-in-out infinite;
}

.lights {
  width: 100%;
  height: 200px;
  background: url('lights.png') repeat-x;
  background-size: contain;
  animation: sparkle 2s infinite linear;
}

.love-message {
  font-size: 36px;
  color: #ff69b4;
  margin-top: 20px;
}

@keyframes floatUp {
  0% { transform: translateY(50px); opacity: 0; }
  50% { opacity: 1; }
  100% { transform: translateY(-100px); opacity: 0; }
}

@keyframes sparkle {
  from { background-position: 0 0; }
  to { background-position: 100% 0; }
}

document.getElementById('openCard').addEventListener('click', () => {
  document.getElementById('openCard').classList.add('hidden');
  document.getElementById('message').classList.remove('hidden');
});

document.getElementById('yesButton').addEventListener('click', () => {
  document.getElementById('message').classList.add('hidden');
  document.getElementById('animation').classList.remove('hidden');
});

document.getElementById('noButton').addEventListener('click', () => {
  alert('Aww, I still love you!');
});
