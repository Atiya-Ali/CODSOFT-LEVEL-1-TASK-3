# CODSOFT-LEVEL-1-TASK-3
#HTML CODE
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Basic Calculator</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <div class="calculator">
    <input type="text" id="display" disabled>
    <div class="buttons">
      <button onclick="addToDisplay('1')">1</button>
      <button onclick="addToDisplay('2')">2</button>
      <button onclick="addToDisplay('3')">3</button>
      <button onclick="addToDisplay('+')">+</button>
      <button onclick="addToDisplay('4')">4</button>
      <button onclick="addToDisplay('5')">5</button>
      <button onclick="addToDisplay('6')">6</button>
      <button onclick="addToDisplay('-')">-</button>
      <button onclick="addToDisplay('7')">7</button>
      <button onclick="addToDisplay('8')">8</button>
      <button onclick="addToDisplay('9')">9</button>
      <button onclick="addToDisplay('*')">*</button>
      <button onclick="addToDisplay('0')">0</button>
      <button onclick="clearDisplay()">C</button>
      <button onclick="calculate()">=</button>
      <button onclick="addToDisplay('/')">/</button>
    </div>
  </div>
  <script src="script.js"></script>
</body>
</html>



# CSS CODE
.calculator {
    width: 200px;
    margin: 0 auto;
    padding: 20px;
    border: 1px solid #ccc;
    border-radius: 5px;
  }
  
  .buttons {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    grid-gap: 5px;
  }
  
  button {
    padding: 10px;
    font-size: 16px;
  }
  

  # JAVASCRPT CODE
  let displayValue = '';

function addToDisplay(value) {
  displayValue += value;
  document.getElementById('display').value = displayValue;
}

function clearDisplay() {
  displayValue = '';
  document.getElementById('display').value = '';
}

function calculate() {
  try {
    let result = eval(displayValue);
    document.getElementById('display').value = result;
    displayValue = '';
  } catch (error) {
    document.getElementById('display').value = 'Error';
    displayValue = '';
  }
}

