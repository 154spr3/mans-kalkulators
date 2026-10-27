<!DOCTYPE html>
<html lang="lv">
<head>
    <meta charset="UTF-8">
    <title>Mans kalkulators</title>
    <style>
        body {
            font-family: Arial;
            text-align: center;
            background: lightblue;
            padding: 40px;
        }
        .kalkulators {
            background: white;
            padding: 25px;
            margin: auto;
            max-width: 300px;
            border-radius: 15px;
        }
        input {
            padding: 10px;
            margin: 5px;
            width: 80%;
        }
        button {
            padding: 12px;
            margin: 5px;
            background: blue;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
    </style>
</head>
<body>

<div class="kalkulators">
    <h1>Mans kalkulators</h1>

    <input type="number" id="a" placeholder="Pirmais skaitlis">
    <input type="number" id="b" placeholder="Otrais skaitlis">

    <br>
    <button onclick="rekins('+')">+</button>
    <button onclick="rekins('-')">-</button>
    <button onclick="rekins('*')">×</button>
    <button onclick="rekins('/')">÷</button>

    <h3>Rezultāts:</h3>
    <p id="rezultats">?</p>
</div>

<script>
function rekins(darbiba) {
    let a = Number(document.getElementById("a").value);
    let b = Number(document.getElementById("b").value);
    let r;

    if (darbiba == '+') r = a + b;
    if (darbiba == '-') r = a - b;
    if (darbiba == '*') r = a * b;
    if (darbiba == '/') {
        r = b == 0 ? "Ar nulli dalīt nedrīkst!" : a / b;
    }

    document.getElementById("rezultats").innerText = r;
}
</script>

</body>
</html>
