# calculadora-funcional
Calculadora Funcional

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Calculadora</title>
<style>
    body {
        font-family: Arial, sans-serif;
        background-color: black;
    }

    .calculator {
        width: 300px;
        margin: 100px auto;
        background-color: orange;
        border-radius: 10px;
        padding: 20px;
        box-shadow: 0 0 20px rgba(0, 0, 0, 0.5);
    }
    
    .calculator input[type="button"] {
        width: 70px;
        height: 70px;
        font-size: 24px;
        margin: 5px;
        border: none;
        border-radius: 5px;
        background-color: white;
        color: black;
        cursor: pointer;
    }
    
    .result {
        font-size: 36px;
        text-align: right;
        margin-bottom: 10px;
        color: white;
    }
</style>
</head>
<body>

<div class="calculator">
    <div class="result" id="result">0</div>
    <input type="button" value="7" onclick="addToResult('7')">
    <input type="button" value="8" onclick="addToResult('8')">
    <input type="button" value="9" onclick="addToResult('9')">
    <input type="button" value="/" onclick="addToResult('/')">
    <br>
    <input type="button" value="4" onclick="addToResult('4')">
    <input type="button" value="5" onclick="addToResult('5')">
    <input type="button" value="6" onclick="addToResult('6')">
    <input type="button" value="*" onclick="addToResult('*')">
    <br>
    <input type="button" value="1" onclick="addToResult('1')">
    <input type="button" value="2" onclick="addToResult('2')">
    <input type="button" value="3" onclick="addToResult('3')">
    <input type="button" value="-" onclick="addToResult('-')">
    <br>
    <input type="button" value="0" onclick="addToResult('0')">
    <input type="button" value="." onclick="addToResult('.')">
    <input type="button" value="C" onclick="clearResult()">
    <input type="button" value="+" onclick="addToResult('+')">
    <br>
    <input type="button" value="=" onclick="calculate()">
</div>

<script>
    function addToResult(value) {
        document.getElementById('result').innerText += value;
    }

    function clearResult() {
        document.getElementById('result').innerText = '0';
    }
    
    function calculate() {
        try {
            var result = eval(document.getElementById('result').innerText);
            document.getElementById('result').innerText = result;
        } catch (error) {
            document.getElementById('result').innerText = 'Error';
        }
    }
</script>

</body>
</html>