<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Simple Calculator</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="calculator">
        <input type="text" id="display" disabled> <!-- Display for input and results -->
        <div class="buttons">
            <!-- Numbers -->
            <button class="btn number" data-value="7">7</button>
            <button class="btn number" data-value="8">8</button>
            <button class="btn number" data-value="9">9</button>

            <button class="btn number" data-value="4">4</button>
            <button class="btn number" data-value="5">5</button>
            <button class="btn number" data-value="6">6</button>

            <button class="btn number" data-value="1">1</button>
            <button class="btn number" data-value="2">2</button>
            <button class="btn number" data-value="3">3</button>

            <button class="btn number zero" data-value="0">0</button>
            <button class="btn number" data-value=".">.</button>

            <!-- Operators -->
            <button class="btn operator" data-value="+">+</button>
            <button class="btn operator" data-value="-">-</button>
            <button class="btn operator" data-value="*">&times;</button> <!-- Using HTML entity for multiplication -->
            <button class="btn operator" data-value="/">&divide;</button> <!-- Using HTML entity for division -->

            <!-- Control Buttons -->
            <button class="btn clear" data-value="C">C</button>
            <button class="btn equals" data-value="=">=</button>
        </div>
    </div>

    <script src="script.js"></script>
</body>
</html>
