# PRODIGY_AD_01
BASIC ARITHMETIC CALCULATOR 

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Basic Calculator</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #698fb5;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }
    .calculator {
      background: #ffffff82;
      padding: 20px;
      border-radius: 15px;
      box-shadow:0 0 15px rgba(0,0,0,0.2);
      box-shadow: #3c7e4c;
    
    }
    input[type="text"] {
      width: 90%;
      font-size: 24px;
      padding: 10px;
      margin-bottom: 15px;
      text-align: right;
    }
    .buttons button {
      width: 60px;
      height: 60px;
      font-size: 20px;
      margin: 5px;
      border: none;
      border-radius: 10px;
      cursor: pointer;
    }
    .buttons button.operator {
      background-color: #214a75;
      color: white;
    }
    .buttons button.equal {
      
      background-color: #3c7e4c;
      color: white;
      width: 130px;
    }
    .buttons button.clear {
      background-color: #5f363a;
      color: white;
      width: 130px;
    }
  </style>
</head>
<body>
  <div class="calculator">
    <input type="text" id="display" >
    <div class="buttons">
      <button onclick="appendNumber('7')">7</button>
      <button onclick="appendNumber('8')">8</button>
      <button onclick="appendNumber('9')">9</button>
      <button class="operator" onclick="appendOperator('+')">+</button><br>

      <button onclick="appendNumber('4')">4</button>
      <button onclick="appendNumber('5')">5</button>
      <button onclick="appendNumber('6')">6</button>
      <button class="operator" onclick="appendOperator('-')">-</button><br>

      <button onclick="appendNumber('1')">1</button>
      <button onclick="appendNumber('2')">2</button>
      <button onclick="appendNumber('3')">3</button>
      <button class="operator" onclick="appendOperator('*')">*</button><br>

      <button onclick="appendNumber('0')">0</button>
      <button onclick="appendDot()">.</button>
      <button onclick="clearInterval()">DEL</button>
      <button class="operator" onclick="appendOperator('/')">/</button><br>
      <button class="equal" onclick="calculate()">=</button>

      <button class="clear" onclick="clearDisplay()">C</button>
    </div>
  </div>

  <script>
    let display = document.getElementById('display');

    function appendNumber(number) {
      display.value += number;
    }

    function appendOperator(operator) {
      display.value += operator;
    }

    function appendDot() {
      display.value += '.';
    }

    function clearDisplay() {
      display.value = '';
    }

    function calculate() {
      try {
        display.value = eval(display.value);
      } catch (error) {
        alert('Invalid Expression');
      }
    }
  </script>
</body>
</html>
