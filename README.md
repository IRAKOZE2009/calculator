<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Calculator</title>
  <style>
    body {
      display: flex;
      justify-content: center;
      background: #000000;
    }

    .calculator {
      background: #413358;
      padding: 90px;
      border-radius: 10px;
    }

    .display {
      width: 100%;
      height: 50px;
      margin-bottom: 10px;
      background: #050505;
    }

    .buttons {
      display: grid;
      grid-template-columns: repeat(4, 60px);
      gap: 10px;
    }

    button {
      height: 50px;
      font-size: 1.3em;
      border: none;
      border-radius: 30px;
      cursor: pointer;
      background: #444;
      color: rgb(250, 250, 250);
    }

   .operator {
      background: #93b358;
    }

    .equal {
      background: #3d668d;
    }

    
  </style>
</head>
<body>

<div class="calculator">
  <input type="text" id="display" class="display" disabled>

  <div class="buttons">
    <button onclick="clearDisplay()" class="clear">AC</button>
  <button onclick="clearDisplay()" class="clear">DEL</button>
    <button onclick="appendValue('%')" class="operator">%</button>
    <button onclick="appendValue('/') " class="operator">/</button>
    
    <button onclick="appendValue('*')" class="operator">*</button>
   <button onclick="appendValue('-')" class="operator">-</button>
     <button onclick="appendValue('+')" class="operator">+</button>
   <button onclick="calculate()" class="equal">=</button>
    <button onclick="appendValue('9')">9</button>
    <button onclick="appendValue('8')">8</button>
  <button onclick="appendValue('7')">7</button>
 
 <button onclick="appendValue('6')">6</button>
    <button onclick="appendValue('5')">5</button>
   <button onclick="appendValue('4')">4</button>
  

    <button onclick="appendValue('3')">3</button>
    <button onclick="appendValue('2')">2</button>
    <button onclick="appendValue('1')">1</button>

    <button onclick="appendValue('0')">0</button>
    <button onclick="appendValue('00')">00</button>
    <button onclick="appendValue('.')">.</button>
 
  </div>
</div>

<script>
  function appendValue(value) {
    document.getElementById("display").value += value;
  }

  function clearDisplay() {
    document.getElementById("display").value = "";
  }

  function calculate() {
    try {
      document.getElementById("display").value = eval(document.getElementById("display").value);
    } catch {
      alert("Invalid calculation");
    }
  }
</script>
<script src="script.js"></script>
</body>
</html>
