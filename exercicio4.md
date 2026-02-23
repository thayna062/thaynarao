<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <title>Exemplos do Objeto Math</title>

    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            padding: 20px;
            text-align: center;
        }

        .container {
            background: white;
            padding: 20px;
            border-radius: 10px;
            width: 400px;
            margin: auto;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }

        input {
            padding: 8px;
            width: 80%;
            margin-bottom: 10px;
        }

        button {
            padding: 8px 15px;
            margin: 5px;
            border: none;
            background-color: #007bff;
            color: white;
            cursor: pointer;
            border-radius: 5px;
        }

        button:hover {
            background-color: #0056b3;
        }

        #resultado {
            margin-top: 15px;
            font-weight: bold;
        }
    </style>
</head>

<body>

<div class="container">
    <h2>Calculadora - Objeto Math</h2>

    <input type="number" id="numero" placeholder="Digite um número">

    <br>

    <button onclick="valorAbsoluto()">Valor Absoluto</button>
    <button onclick="raizQuadrada()">Raiz Quadrada</button>
    <button onclick="potencia()">Elevado ao Quadrado</button>
    <button onclick="arredondarCima()">Arredondar ↑</button>
    <button onclick="arredondarBaixo()">Arredondar ↓</button>
    <button onclick="numeroAleatorio()">Número Aleatório</button>

    <div id="resultado"></div>
</div>

<script>

function pegarNumero() {
    return parseFloat(document.getElementById("numero").value);
}

function valorAbsoluto() {
    let num = pegarNumero();
    document.getElementById("resultado").innerText =
        "Valor absoluto: " + Math.abs(num);
}

function raizQuadrada() {
    let num = pegarNumero();
    document.getElementById("resultado").innerText =
        "Raiz quadrada: " + Math.sqrt(num);
}

function potencia() {
    let num = pegarNumero();
    document.getElementById("resultado").innerText =
        "Elevado ao quadrado: " + Math.pow(num, 2);
}

function arredondarCima() {
    let num = pegarNumero();
    document.getElementById("resultado").innerText =
        "Arredondado para cima: " + Math.ceil(num);
}

function arredondarBaixo() {
    let num = pegarNumero();
    document.getElementById("resultado").innerText =
        "Arredondado para baixo: " + Math.floor(num);
}

function numeroAleatorio() {
    document.getElementById("resultado").innerText =
        "Número aleatório (0 a 100): " + Math.floor(Math.random() * 101);
}

</script>

</body>
</html>
