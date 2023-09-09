<title>WAZE</title>
<body>
    <main>
        <div class="mainBox">
            <div class="center">
                <div class="track">
                    <div class="cart">🚗</div>
                    <div class="sky"></div>
                    <div class="grass"></div>
                    <div class="grass2"></div>
                    <div class="grass3"></div>
                    <div class="grass4"></div>
                </div>
            </div>
            <h1 class="title">WAZE PARTICULAR</h1>
            <div class="menu">
                <a href="/cidade1-inicio" class="btn">Cidade 1</a>
                <a href="/cidade2-inicio" class="btn">Cidade 2</a>
                <a href="/cidade3-inicio" class="btn">Cidade 3</a>
                <a href="/criar" class="btn">Criar Cidade</a>
                <a href="/sobre" class="btn">Sobre</a>
            </div>
        </div>
    </main>
</body>

<div class="notFooter">
    Copyright © Kerou & Iain
</div>

<style>
    body {
        display: flex;
        justify-content: center;
        align-items: center;
        height: 100vh;
        margin: 0;
    }
    .center{
        display: flex;
        justify-content: center;
        align-items: center;

    }
    .track {
        width: 250px;
        height: 40px;
        background-color: #444;
        position: relative;
    }
    .track::before {
        content: '';
        width: 30px;
        height: 8px;
        background-color: #fff;
        position: absolute;
        top: 15px;
    }
    .track::before {
        right: 35%;
    }
    .cart {
        font-size:40px;
        width: 50px;
        height: 30px;
        border-radius: 50%;
        position: absolute;
        top: -25px;
        right: 0;
        animation: moveCart 3s linear infinite;
    }
    @keyframes moveCart {
        0% {
            right: 0;
        }
        100% {
            right: calc(100% - 30px);
        }
    }
    .grass {
        background-color: rgb(61, 116, 25);
        height: 10px;
        width: 15px;
        position: absolute;
        top: -10px; /* Posição da grama em relação ao topo */
    }
    .grass2 {
        background-color: green;
        height: 10px;
        width: 24px;
        position: absolute;
        top: -10px; /* Posição da grama em relação ao topo */
        left: 50px;
    }
    .grass3 {
        background-color: rgb(61, 116, 25);
        height: 10px;
        width: 40px;
        position: absolute;
        top: -10px; /* Posição da grama em relação ao topo */
        left: 120px;
    }
    .grass4 {
        background-color: green;
        height: 10px;
        width: 24px;
        position: absolute;
        top: -10px; /* Posição da grama em relação ao topo */
        left: 200px;
    }
    .sky{
        background-color: rgba(192, 225, 255); 
        height: 20px;
        width: 250px;
        position: absolute;
        top: -20px; 
        left: 0px;
    }

    .mainBox {
        text-align: center;
        background-color: rgba(223, 240, 255, 0.7); 
        padding: 20px;
        width: 460px;
        border-radius: 10px;
    }

    h1 {
        font-size: 36px;
        color: #333;
    }

    .btn {
        display: block;
        background: #5776cc;
        color: white;
        margin: 10px auto; 
        padding: 10px 20px;
        font-weight: bold;
        width: 200px;
        border: none;
        border-radius: 5px;
        font-size: 18px;
        cursor: pointer;
        text-decoration: none;
    }

    .btn:hover {
        opacity: 0.8; 
    }

    .notFooter {    
        position: fixed;
        bottom: 0;
        width: 97.9%;
        text-align: center;
        background-color: rgba(192, 225, 255, 0.7); 
        padding: 20px;
    }
</style>