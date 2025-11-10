<!DOCTYPE html>
<html>
<head>
  <title>Ad Countdown on Image Click</title>
  <style>
    #adSection { display: none; }
    #timer { font-size: 2em; margin: 20px; }
  </style>
</head>
<body>
  <!-- Replace 'your-image.jpg' with your actual image name -->
  <img id="clickableImage" src="![Uploading image.png…]()
" alt="Click Me" style="cursor:pointer; max-width: 300px;" />

  <div id="timer"></div>
  <div id="adSection">
    <!-- Place your ad code here (image, video, or iframe, etc.) -->
    <h2>Your Advertisement</h2>
    <img src="ad-image.jpg" alt="Ad">
  </div>

  <script>
    var image = document.getElementById('clickableImage');
    var timerDisplay = document.getElementById('timer');
    var adSection = document.getElementById('adSection');

    image.onclick = function() {
      image.style.display = 'none';      // Hide image
      var countdown = 10;                // Start from 10 seconds
      timerDisplay.innerHTML = "Ad will start in " + countdown + " seconds...";
      var interval = setInterval(function() {
        countdown--;
        timerDisplay.innerHTML = "Ad will start in " + countdown + " seconds...";
        if (countdown <= 0) {
          clearInterval(interval);
          timerDisplay.style.display = 'none';
          adSection.style.display = 'block'; // Show ad
        }
      }, 1000);
    };
  </script>
</body>
</html>
