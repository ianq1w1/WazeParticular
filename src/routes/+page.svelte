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
                <a href="/cidade1-inicio" class="btn"><b>Cidade:</b> Igarassu</a>
                <a href="/cidade2-inicio" class="btn"><b>Cidade:</b> Paulista</a>
                <!--<a href="/cidade3-inicio" class="btn">Cidade 3</a>-->
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
        background-color: rgba(223, 240, 255); 
        padding: 40px 30px;
        width: 460px;
        border-radius: 10px;
    }

    h1 {
        font-size: 40px;    
        color: #333333;
        text-shadow: 2px 2px 0px #FFFFFF, 5px 4px 0px rgba(0,0,0,0.15);
        color: #333333;
        margin-bottom: 0;
    }
    

    .btn {
        display: block;
        background: #5d7fdb;
        color: white;
        margin: 10px auto; 
        padding: 10px 20px;
        width: 200px;
        border: none;
        border-radius: 5px;
        font-size: 18px;
        cursor: pointer;
        text-decoration: none;
        position: relative;
    }

    .btn::before {
        content: "";
        position: absolute;
        top: 50%;
        right: 10px;
        width: 0;
        height: 0;
        border-style: solid;
        border-width: 8px 0 8px 10px;
        border-color: transparent transparent transparent #475b94; /* Cor da seta quando o mouse está sobre o botão */
        transform: translateY(-50%);
        transition: border-color 0.3s ease-in-out;
    }
    .btn:hover {
        background: #475b94;
    }
    .btn:hover::before {
        border-color: transparent transparent transparent white; /* Cor da seta quando o mouse está sobre o botão */
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