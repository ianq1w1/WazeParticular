<body>
    <div class="container">
        <h1>📚 Sobre o projeto</h1>
        <hr>
        <div class="content">
            Projeto feito por Carolayne e Ian para a disciplina de Algoritmos e Estruturas de Dados.
            <br>
            <br>
            Fazendo referência com o app de GPS waze, o projeto tem como objetivo mostrar o caminho mais rápido para o usuário chegar ao seu destino.
            <br>
            <br>
            <div class="haha">
                <b>Spoiler:</b> Deu Ruim!
            </div>
        </div>
        <div class="pastinha">
            <a href="/" class="btn">🏠 Voltar para a Home</a>
        </div>
    </div>
</body>

<style>
    body {
        display: flex;
        justify-content: center;
        align-items: center;
        height: 100vh;
        width: 100vw;
        margin: auto;
        position: relative;
    }

    body::before {
        content: '';
        background-image: url('https://i.pinimg.com/originals/e0/7e/a2/e07ea2eda9d787e4de5bfce55fd70f2c.jpg');
        background-size: cover;
        filter: blur(10px); 
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        z-index: -1;
    }

    .container {
        max-width: 600px;
        padding: 20px 60px;
        background-color: #fff;
        border-radius: 10px;
        box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
    }

    h1 {
        font-size: 35px;
        font-family: 'Courier New', Courier, monospace;
        color: #333;
        margin-bottom: 0;
    }

    .content {
        font-size: 20px;
        color: #555;
        margin: 20px 0;
    }

    .pastinha{
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .btn{
        display: flex;
        justify-content: center;
        background: #5776cc;
        color: white;
        margin: 10px;
        padding: 10px 30px;
        border: none;
        border-radius: 5px;
        font-size: 18px;
        cursor: pointer;
        text-decoration: none;
    }

    .btn:hover{
        background-color: #3754a3;
    }

    .haha{
        text-align: right;
        text-decoration: line-through;
        font-size: 15px;
    }
</style>