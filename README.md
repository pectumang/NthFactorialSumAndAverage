<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Loop Operations</title>

    <style>
        body {
            font-family: 'Arial', sans-serif;
            background-color: #3498db; /* Blue background */
            text-align: center;
            color: white; /* White text */
            margin: 50px;
        }

        h2 {
            color: #fff; /* White text */
        }

        label {
            font-size: 16px;
            margin-right: 10px;
            color: #fff; /* White text */
        }

        input {
            padding: 10px;
            font-size: 16px;
            border: 1px solid #fff; /* White border */
            border-radius: 5px;
            background-color: #fff; /* White background */
            color: #3498db; /* Blue text */
            margin-bottom: 10px;
        }

        button {
            padding: 10px;
            font-size: 16px;
            border: 1px solid #fff; /* White border */
            border-radius: 5px;
            background-color: #fff; /* White background */
            color: #3498db; /* Blue text */
            cursor: pointer;
        }

        button:hover {
            background-color: #2980b9; /* Slightly darker blue on hover */
        }

        h3 {
            color: #fff; /* White text */
        }

        #factorialResult, #sumResult, #averageResult {
            font-size: 18px;
        }
    </style>
</head>
<body>

    <h2>Loop Operations</h2>

    <label for="numberInput">Enter a number (n): </label>
    <br>
    <input type="number" id="numberInput" min="1" step="1">
    <br>
    <button onclick="calculateResults()">Calculate</button>

    <h3>Results:</h3>
    <p id="factorialResult"></p>
    <p id="sumResult"></p>
    <p id="averageResult"></p>

    <script>
        function calculateResults() {
            // Get the input value
            const n = parseInt(document.getElementById('numberInput').value);

            // Calculate the nth factorial using a While Loop
            let factorial = 1;
            let i = 1;
            while (i <= n) {
                factorial *= i;
                i++;
            }
            document.getElementById('factorialResult').textContent = `Factorial(${n}) = ${factorial}`;

            // Calculate the sum of the first n numbers using a Do While Loop
            let sum = 0;
            i = 1;
            do {
                sum += i;
                i++;
            } while (i <= n);
            document.getElementById('sumResult').textContent = `Sum of first ${n} numbers = ${sum}`;

            // Calculate the average of the first n numbers using a For Loop
            let total = 0;
            for (i = 1; i <= n; i++) {
                total += i;
            }
            const average = total / n;
            document.getElementById('averageResult').textContent = `Average of first ${n} numbers = ${average.toFixed(2)}`;
        }
    </script>

</body>
</html>
