# Compliment Generator8 <3
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
            justify-content: flex-start; 
            align-items: center;
            min-height: 100vh;
            margin: 0;
            padding-left: 2rem; 
            box-sizing: border-box;
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
        /* CHANGED: Adjusted to display the two words side-by-side nicely */
        .results-container {
            display: flex;
            gap: 10px;
            margin-top: 1.5rem;
        }
        .result-box {
            flex: 1;
            padding: 15px;
            background-color: #ecf0f1;
            border-left: 5px solid #3498db;
            border-radius: 4px;
            min-height: 24px;
            font-size: 1.1rem;
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
    
    <label for="wordPool2">Enter your words2 (separated by commas):</label>
    <textarea id="wordPool2" placeholder="e.g. Apple2, Banana2, Orange2, Pineapple2, Grape2">Apple, Banana, Orange, Pineapple, Grape</textarea>
    
    <button onclick="generateWords()">Generate 2 Random Words</button>
    
    <div class="results-container">
        <div class="result-box" id="resultDisplay1">Word 1</div>
        <div class="result-box" id="resultDisplay2">Word 2</div>
    </div>
</div>

<script>
function generateWords() {
    const inputText = document.getElementById('wordPool').value;
    const inputText2 = document.getElementById('wordPool2').value;
    
    const wordList = inputText.split(',')
                              .map(word => word.trim())
                              .filter(word => word.length > 0);
    const wordList2 = inputText.split(',')
                              .map(word => word.trim())
                              .filter(word => word.length > 0);
    
    // Check if the user provided enough words
    if (wordList.length < 2) {
        document.getElementById('resultDisplay1').innerText = "❌ Please enter";
        document.getElementById('resultDisplay2').innerText = "at least 2 words!";
        return;
    }
    
    // Pick the first random word
    const index1 = Math.floor(Math.random() * wordList.length);
    const word1 = wordList[index1];
    
    // Pick the second random word from the remaining options
    const index2 = Math.floor(Math.random() * wordList2.length);
    const word2 = wordList2[index2];
    
    // Output the words to their respective text boxes
    document.getElementById('resultDisplay1').innerText = word1;
    document.getElementById('resultDisplay2').innerText = word2;
}
</script>

</body>
</html>
