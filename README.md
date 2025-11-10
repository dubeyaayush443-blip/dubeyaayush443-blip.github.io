<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ad Trigger Page</title>
    <link rel="stylesheet" href="css/style.css">
</head>
<body>

    <div class="main-content">
        <div class="container">
            <h1>Welcome to My Page!</h1>
            <p>Click on the image below to start the ad countdown.</p>

            <!-- Replace 'images/your-image.jpg' with the path to your image -->
            <img id="triggerImage" src="images/your-image.jpg" alt="Clickable Image">

            <p>Or click anywhere else on the page to trigger the ad.</p>
        </div>
    </div>

    <!-- Ad Overlay -->
    <div id="adOverlay" class="ad-overlay">
        <div class="ad-content">
            <h2>Advertisement</h2>
            <!-- Placeholder for ad content -->
            <div class="ad-placeholder">
                <p>Your Ad Goes Here</p>
                <p><em>(This could be an image, text, or a link)</em></p>
            </div>
            <p>Please wait <span id="countdown">10</span> seconds.</p>
            <div id="adTimerBar"></div>
            <button id="skipAdButton">Skip Ad</button>
        </div>
    </div>

    <script src="js/script.js"></script>
</body>
</html>
