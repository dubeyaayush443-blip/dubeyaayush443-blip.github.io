<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Clickable Image Timer</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            background-color: #f4f4f4;
            margin: 0;
        }

        .container {
            text-align: center;
            position: relative; /* Needed for absolute positioning of the text */
        }

        #myImage {
            width: 300px; /* Adjust image size as needed */
            height: auto;
            cursor: pointer; /* Indicates it's clickable */
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            transition: transform 0.3s ease; /* Smooth transition for hover effect */
        }

        #myImage:hover {
            transform: scale(1.05); /* Slight zoom on hover */
        }

        #timerText {
            position: absolute;
            top: -40px; /* Position above the image */
            left: 50%;
            transform: translateX(-50%);
            font-size: 1.5em;
            color: #333;
            background-color: rgba(255, 255, 255, 0.8);
            padding: 10px 15px;
            border-radius: 5px;
            opacity: 0; /* Hidden by default */
            visibility: hidden; /* Also hidden */
            transition: opacity 0.5s ease, visibility 0.5s ease; /* Smooth fade-in */
        }

        #timerText.visible {
            opacity: 1;
            visibility: visible;
        }

        /* Optional: Style for when the timer is active to disable further clicks if needed */
        .container.timer-active #myImage {
            cursor: not-allowed; /* Indicate it's not clickable during timer */
            opacity: 0.7;
        }
    </style>
</head>
<body>
    <div class="container">
        <div id="timerText">Wait for 10 seconds</div>
        <img id="myImage" src="https://via.placeholder.com/300x200/007bff/ffffff?text=Click+Me" alt="Clickable Image">
    </div>

    <script>
        const image = document.getElementById('myImage');
        const timerText = document.getElementById('timerText');
        const container = document.querySelector('.container'); // Get the container

        let timerActive = false; // Flag to prevent multiple timers from starting

        image.addEventListener('click', function() {
            // Prevent starting new timers if one is already running
            if (timerActive) {
                return;
            }

            timerActive = true; // Set the flag to true
            container.classList.add('timer-active'); // Add class for styling

            // Show the timer text
            timerText.classList.add('visible');

            // Start the 10-second timer
            setTimeout(function() {
                // Hide the timer text after 10 seconds
                timerText.classList.remove('visible');

                // Reset the flag and container class after the timer finishes
                timerActive = false;
                container.classList.remove('timer-active');

                // Optional: You can add more actions here after the timer ends
                console.log("Timer finished!");
                // Example: Re-enable clicking or change the image
                // image.style.cursor = 'pointer';
            }, 10000); // 10000 milliseconds = 10 seconds
        });
    </script>
</body>
</html>
