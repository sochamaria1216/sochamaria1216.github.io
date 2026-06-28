# Compliment Generator <3
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Custom Word Generator</title>
    <style>
        body {
            font-family: system-ui, -apple-system, sans-serif;
            background-color: #f4f4f9;
            color: #333;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            margin: 0;
        }
        .container {
            background: white;
            padding: 2rem;
            border-radius: 12px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
            width: 100%;
            max-width: 450px;
        }
        h2 {
            margin-top: 0;
            color: #2c3e50;
        }
        label {
            font-weight: bold;
            display: block;
            margin-bottom: 0.5rem;
        }
        textarea {
            width: 100%;
            height: 100px;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 6px;
            box-sizing: border-box;
            resize: vertical;
            font-family: inherit;
        }
        button {
            width: 100%;
            background-color: #3498db;
            color: white;
            border: none;
            padding: 12px;
            font-size: 1rem;
            font-weight: bold;
            border-radius: 6px;
            cursor: pointer;
            margin-top: 1rem;
            transition: background 0.2s;
        }
        button:hover {
            background-color: #2980b9;
        }
        .result-box {
            margin-top: 1.5rem;
            padding: 15px;
            background-color: #ecf0f1;
            border-left: 5px solid #3498db;
            border-radius: 4px;
            min-height: 24px;
            font-size: 1.2rem;
            font-weight: bold;
            text-align: center;
            word-wrap: break-word;
        }
    </style>
</head>
<body>

<div class="container">
    <h2>Word Generator</h2>
    
    <label for="wordPool">Enter your words (separated by commas):</label>
    <textarea id="wordPool" placeholder="e.g. Apple, Banana, Orange, Pineapple, Grape">Apple, Banana, Orange, Pineapple, Grape</textarea>
    
    <button onclick="generateWord()">Generate Random Word</button>
    
    <div class="result-box" id="resultDisplay">Click the button to start!</div>
</div>

<script>
function generateWord() {
    // 1. Get the text from the textarea
    const inputText = document.getElementById('wordPool').value;
    
    // 2. Split the text into an array using commas, and clean up extra spaces
    const wordList = inputText.split(',')
                              .map(word => word.trim())
                              .filter(word => word.length > 0);
    
    // 3. Handle the edge case where the box is empty
    if (wordList.length === 0) {
        document.getElementById('resultDisplay').innerText = "❌ Please enter some words first!";
        return;
    }
    
    // 4. Pick a random index using the formula: Math.floor(Math.random() * length)
    const randomIndex = Math.floor(Math.random() * wordList.length);
    const chosenWord = wordList[randomIndex];
    
    // 5. Display the chosen word on the screen
    document.getElementById('resultDisplay').innerText = chosenWord;
}
</script>
</body>
</html>


<!-- NEW LINE -->



<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Custom Word Generator</title>
    <style>
        body {
            font-family: system-ui, -apple-system, sans-serif;
            background-color: #f4f4f9;
            color: #333;
            display: flex;
            justify-content: left;
            align-items: right;
            min-height: 100vh;
            margin: 0;
        }
        .container {
            background: white;
            padding: 2rem;
            border-radius: 12px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
            width: 100%;
            max-width: 450px;
        }
        h2 {
            margin-top: 0;
            color: #2c3e50;
        }
        label {
            font-weight: bold;
            display: block;
            margin-bottom: 0.5rem;
        }
        textarea {
            width: 100%;
            height: 100px;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 6px;
            box-sizing: border-box;
            resize: vertical;
            font-family: inherit;
        }
        button {
            width: 100%;
            background-color: #3498db;
            color: white;
            border: none;
            padding: 12px;
            font-size: 1rem;
            font-weight: bold;
            border-radius: 6px;
            cursor: pointer;
            margin-top: 1rem;
            transition: background 0.2s;
        }
        button:hover {
            background-color: #2980b9;
        }
        .result-box {
            margin-top: 1.5rem;
            padding: 15px;
            background-color: #ecf0f1;
            border-left: 5px solid #3498db;
            border-radius: 4px;
            min-height: 24px;
            font-size: 1.2rem;
            font-weight: bold;
            text-align: center;
            word-wrap: break-word;
        }
    </style>
</head>
<body>

<div class="container">
    <h2>Word Generator</h2>
    
    <label for="wordPool">Enter your words (separated by commas):</label>
    <textarea id="wordPool" placeholder="e.g. Apple2, Banana2, Orange2, Pineapple2, Grape2">Apple2, Banana2, Orange2, Pineapple2, Grape</textarea>
    
    <button onclick="generateWord()">Generate Random Word</button>
    
    <div class="result-box" id="resultDisplay">Click the button to start!</div>
</div>

<script>
function generateWord() {
    // 1. Get the text from the textarea
    const inputText = document.getElementById('wordPool').value;
    
    // 2. Split the text into an array using commas, and clean up extra spaces
    const wordList = inputText.split(',')
                              .map(word => word.trim())
                              .filter(word => word.length > 0);
    
    // 3. Handle the edge case where the box is empty
    if (wordList.length === 0) {
        document.getElementById('resultDisplay').innerText = "❌ Please enter some words first!";
        return;
    }
    
    // 4. Pick a random index using the formula: Math.floor(Math.random() * length)
    const randomIndex = Math.floor(Math.random() * wordList.length);
    const chosenWord = wordList[randomIndex];
    
    // 5. Display the chosen word on the screen
    document.getElementById('resultDisplay').innerText = chosenWord;
}
</script>
</body>
</html>

