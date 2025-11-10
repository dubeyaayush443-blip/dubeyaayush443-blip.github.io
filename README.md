<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>5-Second Image Timer</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            background-color: #e0f7fa; /* Light cyan background */
            margin: 0;
        }

        .container {
            text-align: center;
            position: relative;
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        #clickableImage {
            width: 350px; /* Larger image */
            height: auto;
            cursor: pointer;
            border-radius: 12px;
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.25);
            transition: transform 0.3s ease-in-out, box-shadow 0.3s ease-in-out;
            margin-top: 30px; /* Space for the timer text */
        }

        #clickableImage:hover {
            transform: translateY(-5px) scale(1.03); /* Lift and slightly enlarge on hover */
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.3);
        }

        #timerDisplay {
            font-size: 1.8em; /* Larger text */
            color: #004d40; /* Dark teal color */
            font-weight: bold;
            margin-bottom: 15px; /* Space between text and image */
            opacity: 0; /* Hidden by default */
            visibility: hidden; /* Also hidden */
            transition: opacity 0.5s ease, visibility 0.5s ease;
            position: absolute; /* Position it above the image */
            top: 10px; /* Adjust as needed */
            left: 50%;
            transform: translateX(-50%);
            background-color: rgba(255, 255, 255, 0.9);
            padding: 12px 20px;
            border-radius: 8px;
            text-shadow: 1px 1px 2px rgba(0,0,0,0.1);
        }

        #timerDisplay.visible {
            opacity: 1;
            visibility: visible;
        }

        /* Styling when the timer is active */
        .container.counting .timer-message {
            color: #d32f2f; /* Red color for active countdown */
        }

        .container.counting #clickableImage {
            cursor: not-allowed; /* Indicates it's temporarily disabled */
            opacity: 0.8;
            box-shadow: 0 6px 12px rgba(255, 0, 0, 0.3); /* Reddish shadow */
        }
    </style>
</head>
<body>
    <div class="container">
        <div id="timerDisplay">
            <span class="timer-message">Click the image to start the 5-second timer!</span>
        </div>
        <img id="clickableImage" src="https://via.placeholder.com/350x250/00bcd4/ffffff?text=Click+Me+for+Timer" alt="Clickable Image for Timer">
    </div>

    <script>
        const clickableImage = document.getElementById('clickableImage');
        const timerDisplay = document.getElementById('timerDisplay');
        const timerMessage = document.querySelector('.timer-message');
        const container = document.querySelector('.container');

        let timerRunning = false; // Flag to prevent multiple timers
        const countdownDuration = 5000; // 5 seconds in milliseconds

        clickableImage.addEventListener('click', function() {
            // If the timer is already running, do nothing
            if (timerRunning) {
                return;
            }

            timerRunning = true; // Mark timer as running
            container.classList.add('counting'); // Add class for visual feedback

            // Change the initial message to "Counting down..."
            timerMessage.textContent = "Counting down...";
            timerDisplay.classList.add('visible'); // Show the timer display

            // Start the 5-second countdown
            const timerInterval = setInterval(function() {
                // This part is not strictly needed for a fixed 5-second timer,
                // but it's useful if you wanted to show remaining seconds.
                // For a fixed 5 seconds, we just need to know when it ends.
            }, 1000); // Update every second (optional for this specific requirement)


            setTimeout(function() {
                // When the 5 seconds are up:
                timerDisplay.classList.remove('visible'); // Hide the timer display
                timerMessage.textContent = "Timer finished!"; // Change message briefly

                // Reset the timer state
                timerRunning = false;
                container.classList.remove('counting');

                // Optionally, reset the message after a short delay
                setTimeout(function() {
                    timerMessage.textContent = "Click the image to start the 5-second timer!";
                    clickableImage.style.cursor = 'pointer'; // Ensure cursor is reset
                    clickableImage.style.opacity = '1'; // Ensure opacity is reset
                }, 1500); // Reset message after 1.5 seconds

                clearInterval(timerInterval); // Clear the interval if it was active
            }, countdownDuration); // Execute after 5000 milliseconds
        });
    </script>
</body>
</html>
