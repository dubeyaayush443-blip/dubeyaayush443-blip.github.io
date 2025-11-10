<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MovieHub - Your Gateway to Films</title>
    <link rel="stylesheet" href="style.css">
    <link href="https://fonts.googleapis.com/css2?family=Open+Sans:wght@300;400;600;700&family=Poppins:wght@400;600;700&display=swap" rel="stylesheet">
</head>
<body>
    <header>
        <div class="container">
            <a href="#" class="logo">MovieHub</a>
            <nav>
                <ul>
                    <li><a href="#">Home</a></li>
                    <li><a href="#">Genres</a></li>
                    <li><a href="#">Search</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <main class="container">
        <section class="hero-section">
            <!-- You could add a featured movie carousel here -->
            <h2 class="section-title">Trending Now</h2>
        </section>

        <section class="movie-list">
            <h2 class="section-title">New Releases</h2>
            <div class="movie-grid">
                <!-- Movie Card 1 -->
                <div class="movie-card">
                    <div class="movie-poster">
                        <img src="" alt="Movie Title 1">
                        <div class="overlay">
                            <a href="#" class="watch-button">Watch Now</a>
                        </div>
                    </div>
                    <div class="movie-info">
                        <h3 class="movie-title">The Quantum Leap</h3>
                        <p class="movie-year">2023</p>
                        <p class="movie-genre">Sci-Fi, Adventure</p>
                    </div>
                </div>

                <!-- Movie Card 2 -->
                <div class="movie-card">
                    <div class="movie-poster">
                        <img src="" alt="Movie Title 2">
                        <div class="overlay">
                            <a href="#" class="watch-button">Watch Now</a>
                        </div>
                    </div>
                    <div class="movie-info">
                        <h3 class="movie-title">Crimson Tide Mystery</h3>
                        <p class="movie-year">2022</p>
                        <p class="movie-genre">Thriller, Mystery</p>
                    </div>
                </div>

                <!-- Add more movie cards here -->
                <div class="movie-card">
                    <div class="movie-poster">
                        <img src="" alt="Movie Title 3">
                        <div class="overlay">
                            <a href="#" class="watch-button">Watch Now</a>
                        </div>
                    </div>
                    <div class="movie-info">
                        <h3 class="movie-title">Galactic Odyssey</h3>
                        <p class="movie-year">2024</p>
                        <p class="movie-genre">Sci-Fi, Space Opera</p>
                    </div>
                </div>

                <div class="movie-card">
                    <div class="movie-poster">
                        <img src="" alt="Movie Title 4">
                        <div class="overlay">
                            <a href="#" class="watch-button">Watch Now</a>
                        </div>
                    </div>
                    <div class="movie-info">
                        <h3 class="movie-title">The Last Samurai</h3>
                        <p class="movie-year">2010</p>
                        <p class="movie-genre">Action, Drama</p>
                    </div>
                </div>

                <!-- Repeat for more movies -->
            </div>
        </section>
    </main>

    <footer>
        <div class="container">
            <p>&copy; 2023 MovieHub. All rights reserved. | <a href="#">Privacy Policy</a> | <a href="#">Terms of Service</a></p>
        </div>
    </footer>

    <script src="script.js"></script>
</body>
</html>
