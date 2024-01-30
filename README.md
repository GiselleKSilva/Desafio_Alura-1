#challengeonedecodificador5

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Custom Encryption</title>
</head>
<body>
  <h1>Custom Encryption</h1>

  <label for="inputText">Enter Text: </label>
  <textarea id="inputText" rows="4" cols="50"></textarea>
  
  <br>

  <button onclick="encrypt()">Encrypt</button>

  <br>

  <label for="outputText">Result: </label>
  <textarea id="outputText" rows="4" cols="50" readonly></textarea>

  <script>
    function encrypt() {
      const inputText = document.getElementById('inputText').value;
      const encryptedText = customEncrypt(inputText);
      document.getElementById('outputText').value = encryptedText;
    }

    function customEncrypt(text) {
      const encryptionRules = {
        'e': 'enter',
        'i': 'imes',
        'a': 'ai',
        'o': 'ober',
        'u': 'ufat'
      };

      // Convertendo o texto de acordo com as regras de criptografia
      const encryptedText = text.replace(/[eioua]/g, match => encryptionRules[match] || match);

      return encryptedText;
    }
  </script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Custom Encryption</title>
</head>
<body>
  <h1>Custom Encryption</h1>

  <label for="inputText">Enter Text: </label>
  <textarea id="inputText" rows="4" cols="50"></textarea>
  
  <br>

  <button onclick="encrypt()">Encrypt</button>
  <button onclick="copyText('outputText')">Copy Encrypted</button>

  <br>

  <label for="outputText">Result: </label>
  <textarea id="outputText" rows="4" cols="50" readonly></textarea>

  <script>
    function encrypt() {
      const inputText = document.getElementById('inputText').value;
      const encryptedText = customEncrypt(inputText);
      document.getElementById('outputText').value = encryptedText;
    }

    function customEncrypt(text) {
      const encryptionRules = {
        'e': 'enter',
        'i': 'imes',
        'a': 'ai',
        'o': 'ober',
        'u': 'ufat'
      };

      const encryptedText = text.replace(/[eioua]/g, match => encryptionRules[match] || match);

      return encryptedText;
    }

    function copyText(elementId) {
      const textArea = document.getElementById(elementId);
      textArea.select();
      document.execCommand('copy');
    }
  </script>
</body>
</html>

