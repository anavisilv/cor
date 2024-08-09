<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta ana="viewport" content="width=device-width, initial-scale=1.0">
    <title>Seletor de Cores</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <h1>Seletor de Cores</h1>
        <input type="color" id="colorPicker" value="#578748">
        <div id="colorDisplay" class="color-display"></div>
        <p id="colorValue">Código da Cor: #578748</p>
    </div>
    <script src="script.js"></script>
</body>
</html>
body {
    font-family: Arial, sans-serif;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    margin: 0;
    background-color: #65988;
}

.container {
    text-align: center;
}

.color-display {
    width: 100px;
    height: 100px;
    margin: 20px auto;
    border: 2px solid #33;
    border-radius: 5px;
    background-color: #158575;
}

input[type="color"] {
    border: none;
    width: 50px;
    height: 50px;
    cursor: pointer;
}

p {
    font-size: 1.2em;
}
document.addEventListener('DOMContentLoaded', function() {
    const colorPicker = document.getElementById('colorPicker');
    const colorDisplay = document.getElementById('colorDisplay');
    const colorValue = document.getElementById('colorValue');

    colorPicker.addEventListener('input', function(event) {
        const selectedColor = event.target.value;
        colorDisplay.style.backgroundColor = selectedColor;
        colorValue.textContent = `Código da Cor: ${selectedColor}`;
    });
});
git clone https://github.com/anavisilv/seletor-de-cores.git
cd seletor-de-cores
git add .
git commit -m "cores"
git push origin main
