## Play
Welcome to the **Guess the Number** game! Try to guess the number I'm thinking of between 1 and 100.

<div>
    <input type="number" id="userGuess" placeholder="Enter your guess" min="1" max="100">
    <button onclick="checkGuess()">Guess!</button>
</div>

<div id="result"></div>

<script>
    const randomNumber = Math.floor(Math.random() * 100) + 1;
    let attempts = 0;

    function checkGuess() {
        const userGuess = parseInt(document.getElementById('userGuess').value);
        attempts++;
        const resultDiv = document.getElementById('result');

        if (userGuess < 1 || userGuess > 100) {
            resultDiv.textContent = "Please enter a number between 1 and 100.";
        } else if (userGuess < randomNumber) {
            resultDiv.textContent = "Too low! Try again.";
        } else if (userGuess > randomNumber) {
            resultDiv.textContent = "Too high! Try again.";
        } else {
            resultDiv.textContent = `Congratulations! You've guessed the number ${randomNumber} in ${attempts} attempts.`;
        }
    }
</script>
---

## Instructions

1. Enter your guess in the input box.
2. Click the "Guess!" button to submit.
3. Read the feedback to refine your next guess.

---

