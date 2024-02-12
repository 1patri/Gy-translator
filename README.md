# Gy-translator
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Translator</title>
<style>
    body {
        font-family: Arial, sans-serif;
    }
    #translator {
        margin: 20px;
    }
    textarea {
        width: 100%;
        height: 150px;
        margin-bottom: 10px;
    }
    button {
        padding: 10px 20px;
        background-color: #007bff;
        color: #fff;
        border: none;
        cursor: pointer;
    }
</style>
</head>
<body>
<div id="translator">
    <h2>Translator</h2>
    <textarea id="inputText" placeholder="Enter text to translate"></textarea>
    <button onclick="translate()">Translate</button>
    <textarea id="outputText" placeholder="Translation will appear here" readonly></textarea>
</div>

<script>
    function translate() {
        const inputText = document.getElementById('inputText').value;
        // Here you can implement your translation logic using APIs or any other method
        // For simplicity, let's just reverse the input text
        const translatedText = inputText.split('').reverse().join('');
        document.getElementById('outputText').value = translatedText;
    }
</script>
</body>
</html>
