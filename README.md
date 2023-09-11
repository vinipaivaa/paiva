<!DOCTYPE html>
<html>
<head>
    <title>Pedido de Namoro</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin-top: 50px;
        }
        .button-container {
            position: relative;
        }
        button {
            position: absolute;
        }
    </style>
</head>
<body>
    <h1>Quer namorar comigo?</h1>
    <div class="button-container">
        <button onclick="responder('sim')">Sim</button>
        <button onclick="moverBotao()">Não</button>
    </div>

    <script>
        function responder(resposta) {
            if (resposta === 'sim') {
                alert('Que ótimo! Fico muito feliz! agr pode contaar pra todos ');
            }
        }

        function moverBotao() {
            var botaoNao = document.querySelector('button:last-child');
            var maxX = window.innerWidth - botaoNao.clientWidth;
            var maxY = window.innerHeight - botaoNao.clientHeight;
            var newX = Math.random() * maxX;
            var newY = Math.random() * maxY;
            
            botaoNao.style.left = newX + 'px';
            botaoNao.style.top = newY + 'px';
        }
    </script>
</body>
</html>

