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
