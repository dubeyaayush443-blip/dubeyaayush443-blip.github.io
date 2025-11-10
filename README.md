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
    background-color: #fff;
    padding: 30px;
    border-radius: 8px;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
}

h1 {
    color: #333;
    margin-bottom: 30px;
}

.image-container {
    position: relative; /* Essential for positioning the message */
    display: inline-block; /* So it only takes up the space of the image */
    cursor: pointer; /* Indicates it's clickable */
}

#clickableImage {
    max-width: 100%; /* Make image responsive */
    height: auto;
    display: block; /* Remove extra space below the image */
    border-radius: 5px;
    transition: transform 0.2s ease-in-out; /* Smooth hover effect */
}

#clickableImage:hover {
    transform: scale(1.03); /* Slightly enlarge on hover */
}

.timer-message {
    position: absolute;
    top: 50%; /* Center vertically */
    left: 50%; /* Center horizontally */
    transform: translate(-50%, -50%); /* Actual centering trick */
    background-color: rgba(0, 0, 0, 0.7); /* Semi-transparent black background */
    color: white;
    padding: 15px 25px;
    border-radius: 5px;
    font-size: 1.2em;
    font-weight: bold;
    z-index: 10; /* Ensure it appears above the image */
    opacity: 0; /* Hidden by default */
    transition: opacity 0.3s ease-in-out; /* Smooth fade-in */
}

.timer-message.visible {
    opacity: 1; /* Show the message */
}
