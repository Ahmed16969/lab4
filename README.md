    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lab 4</title>
    <style>
        /* Add any additional styles if needed */
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
        }
        .exercise {
            margin-bottom: 20px;
        }
        hr {
            margin-top: 20px;
            margin-bottom: 20px;
        }
    </style>
</head>
<body>

<!-- Exercise 5.5 & 5.13 -->
<div class="exercise">
    <h2>  - MadLib</h2>
    <!-- Prompt for words -->
    <label for="noun">Enter a noun:</label>
    <input type="text" id="noun" value="animal">

    <label for="adjective">Enter an adjective:</label>
    <input type="text" id="adjective" value="colorful">

    <label for="verb">Enter a verb:</label>
    <input type="text" id="verb" value="jump">

    <label for="adverb">Enter an adverb:</label>
    <input type="text" id="adverb" value="quickly">

    <button onclick="generateMadLib()">Generate MadLib</button>

    <div id="madLibStory"></div>
</div>
<hr>

<!-- Exercise 5.6 -->
<div class="exercise">
    <h2>   Image</h2>
    <img src=http://balance3e.com/Images/mystery.gif alt="Mystery Image">
</div>
<hr>

<!-- Exercise 5.19 & 5.20 -->
<div class="exercise">
    <h2>  Click to Double and Halve</h2>
    <p id="number">10</p>
    <button onclick="doubleNumber()">Click to Double</button>
    <button onclick="halveNumber()">Click to Halve</button>
</div>

<script>
    // JavaScript functions for Exercises
    function generateMadLib() {
        // Get values from input boxes
        var noun = document.getElementById("noun").value;
        var adjective = document.getElementById("adjective").value;
        var verb = document.getElementById("verb").value;
        var adverb = document.getElementById("adverb").value;

        // Build the story
        var story = `Once upon a time, there was a ${adjective} ${noun} that loved to ${verb} ${adverb}.`;

        // Display the story
        document.getElementById("madLibStory").innerHTML = story;
    }

    function doubleNumber() {
        // Get current number value
        var currentNumber = parseFloat(document.getElementById("number").innerText);
        // Double the number
        document.getElementById("number").innerText = currentNumber * 2;
    }

    function halveNumber() {
        // Get current number value
        var currentNumber = parseFloat(document.getElementById("number").innerText);
        // Halve the number
        document.getElementById("number").innerText = currentNumber / 2;
    }
</script>

</body>
</html>
