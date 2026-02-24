<!DOCTYPE html>
<html lang="th">
<head>
  <meta charset="UTF-8">
  <title>เครื่องคิดเลขออนไลน์</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      margin-top: 50px;
    }
    #calculator {
      display: inline-block;
      border: 2px solid #333;
      border-radius: 10px;
      padding: 20px;
      background: #f9f9f9;
    }
    #display {
      width: 220px;
      height: 40px;
      font-size: 20px;
      margin-bottom: 10px;
      text-align: right;
      padding: 5px;
    }
    .button {
      width: 50px;
      height: 50px;
      font-size: 18px;
      margin: 5px;
    }
  </style>
</head>
<body>
  <h2>เครื่องคิดเลขออนไลน์</h2>
  <div id="calculator">
    <input type="text" id="display" disabled>
    <br>
    <button class="button" onclick="press('7')">7</button>
    <button class="button" onclick="press('8')">8</button>
    <button class="button" onclick="press('9')">9</button>
    <button class="button" onclick="press('/')">/</button><br>
    <button class="button" onclick="press('4')">4</button>
    <button class="button" onclick="press('5')">5</button>
    <button class="button" onclick="press('6')">6</button>
    <button class="button" onclick="press('*')">*</button><br>
    <button class="button" onclick="press('1')">1</button>
    <button class="button" onclick="press('2')">2</button>
    <button class="button" onclick="press('3')">3</button>
    <button class="button" onclick="press('-')">-</button><br>
    <button class="button" onclick="press('0')">0</button>
    <button class="button" onclick="press('.')">.</button>
    <button class="button" onclick="calculate()">=</button>
    <button class="button" onclick="press('+')">+</button><br>
    <button class="button" onclick="clearDisplay()">C</button>
  </div>

  <script>
    function press(value) {
      document.getElementById("display").value += value;
    }
    function calculate() {
      try {
        document.getElementById("display").value = 
          eval(document.getElementById("display").value);
      } catch {
        document.getElementById("display").value = "Error";
      }
    }
    function clearDisplay() {
      document.getElementById("display").value = "";
    }
  </script>
</body>
</html>
