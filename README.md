Sure! I can help you create a basic game using HTML. Here's an example of a simple game called "Guess the Number":

```html
<!DOCTYPE html>
<html>
<head>
  <title>Guess the Number</title>
  <style>
    body {
      text-align: center;
      padding-top: 50px;
    }

    h1 {
      color: #333;
    }

    button, input {
      font-size: 18px;
      padding: 10px;
      margin: 10px;
    }
  </style>
</head>
<body>
  <h1>Guess the Number</h1>
  <p>Try to guess the secret number between 1 and 100.</p>
  <input type="number" id="guess" min="1" max="100" required>
  <button type="button" onclick="checkGuess()">Submit</button>
  <p id="message"></p>

  <script>
    // Generate the secret number
    const secretNumber = Math.floor(Math.random() * 100) + 1;

    function checkGuess() {
      // Get the user's guess
      const guess = parseInt(document.getElementById('guess').value);

      // Compare the guess with the secret number
      if (guess === secretNumber) {
        document.getElementById('message').textContent = 'Congratulations! You guessed the number!';
      } else if (guess < secretNumber) {
        document.getElementById('message').textContent = 'Too low! Try a higher number.';
      } else {
        document.getElementById('message').textContent = 'Too high! Try a lower number.';
      }
    }
  </script>
</body>
</html>
```

This simple game generates a secret number between 1 and 100 and prompts the user to guess it. After each guess, the game provides feedback on whether the guess is too high or too low. If the user guesses the correct number, a congratulatory message is displayed.

You can save this code into an HTML file, open it in a web browser, and enjoy playing the "Guess the Number" game. Feel free to customize the HTML and CSS to match your preferences and add additional features as needed. 
