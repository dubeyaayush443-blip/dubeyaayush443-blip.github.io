<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MovieHub - Your Favorite Movies</title>
    <link rel="stylesheet" href="css/style.css">
</head>
<body>

    <header>
        <div class="container">
            <div id="branding">
                <h1>MovieHub</h1>
            </div>
            <nav>
                <ul>
                    <li class="current"><a href="#">Home</a></li>
                    <li><a href="#">Movies</a></li>
                    <li><a href="#">TV Shows</a></li>
                    <li><a href="#">Genres</a></li>
                    <li><a href="#">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <div id="main-content" class="container">
        <section id="showcase">
            <h2>Featured Movies</h2>
            <div class="movie-grid">
                <!-- Example Movie Cards -->
                <div class="movie-card">
                    <img src="" alt="Movie 1 Poster">
                    <h3>Movie Title 1</h3>
                    <p>Action, Adventure</p>
                </div>
                <div class="movie-card">
                    <img src="" alt="Movie 2 Poster">
                    <h3>Movie Title 2</h3>
                    <p>Comedy, Romance</p>
                </div>
                <div class="movie-card">
                    <img src="" alt="Movie 3 Poster">
                    <h3>Movie Title 3</h3>
                    <p>Sci-Fi, Thriller</p>
                </div>
                <div class="movie-card">
                    <img src="" alt="Movie 4 Poster">
                    <h3>Movie Title 4</h3>
                    <p>Drama, Horror</p>
                </div>
                <!-- Add more movie cards as needed -->
            </div>
        </section>
    </div>

    <footer>
        <p>&copy; 2023 MovieHub. All rights reserved.</p>
    </footer>

    <!-- Ad Overlay -->
    <div id="adOverlay" class="ad-overlay">
        <div class="ad-content">
            <h2>Advertisement</h2>
            <p>Please wait <span id="countdown">10</span> seconds.</p>
            <div id="adTimerBar"></div>
            <p><button id="skipAdButton">Skip Ad</button></p>
        </div>
    </div>

    <script src="js/script.js"></script>
</body>
</html>
