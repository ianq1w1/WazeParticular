<script lang="js">




    export let city = [
        [0,0,0,0,0,0,0,0],
        [0,0,1,1,1,1,5,0],
        [0,0,1,0,0,0,1,0],
        [0,0,1,0,0,0,1,0],
        [0,0,1,0,0,0,1,0],
        [0,0,2,1,1,1,1,0],
    ]
 // possivel algoritmo de calculo de rota 
    console.log(city)
 /**
     * @param {number[][]} route
     */
function rota (route){
    var i =0;
    var j = 0;
    var rua = 0

    for(i=0; i<route.length; i++){
        for(j=0; j<route[i].length; j++){
            if(route[i][j] == 1 ){
                rua = route[i][j]
                console.log(route[i][j]);
            }
        }
    }

    var parada = maiorNum(route)
    var partida = carro(route)

    var xcarro = 0;
    var ycarro = 0;

    var xparada = 0;
    var yparada = 0;

//localizar parada e partida 
    for (let i = 0; i < route.length; i++) {
        for (let j = 0; j < route[i].length; j++) {
            if (route[i][j] === partida) {
                xcarro = i;
                ycarro = j;
            }
            if (route[i][j] === parada) {
                xparada = i;
                yparada = j;
            }
        }
    }


    //FUNÇÃO REALOCAR POSIÇÃO DO CARRO 

  /*  for(route[xcarro] != route[xparada]; route[xcarro] <= route[xparada]; xcarro++){
        for(route[ycarro] != route[yparada]; route[ycarro] <= route[yparada]; ycarro++){
            if(route[xcarro][ycarro] <)
        }
    }*/
  /**
   * @param {number} x
   * @param {number} y
   */
    function moveValido(x,y){
    
        return x >= 0 && x < 10 && y >= 0 && y < 10 && route[y][x] !== 1;
    }

    var l = 0;
    var c = 0;
 
    while (xcarro !== xparada || ycarro !== yparada) {
    // Lógica de movimento para direita
    if (xcarro < xparada ) {
        route[ycarro][xcarro] = 0; // Limpa a posição atual do carro
        xcarro++; // Move o carro para a direita
        route[ycarro][xcarro] = partida; // Atualiza a nova posição do carro
    }
    // Lógica de movimento para esquerda
    else if (xcarro > xparada ){
        route[ycarro][xcarro] = 0; // Limpa a posição atual do carro
        xcarro--; // Move o carro para a esquerda
        route[ycarro][xcarro] = partida; // Atualiza a nova posição do carro
    }
    // Lógica de movimento para cima
    else if (ycarro < yparada ){
        route[ycarro][xcarro] = 0; // Limpa a posição atual do carro
        ycarro++; // Move o carro para cima
        route[ycarro][xcarro] = partida; // Atualiza a nova posição do carro
    }
    // Lógica de movimento para baixo
    else if (ycarro > yparada ){
        route[ycarro][xcarro] = 0; // Limpa a posição atual do carro
        ycarro--; // Move o carro para baixo
        route[ycarro][xcarro] = partida; // Atualiza a nova posição do carro
    }

    console.log(route)
}


}


// pega o maior numero da array (objetivo)
/**
     * @param {number[][]} cidade
     */
function maiorNum(cidade){
        let maior = cidade[0][0]; 

        for (let i = 0; i < cidade.length; i++) {
            for(let j = 0; j<cidade[i].length; j++){
                if(cidade[i][j] > maior){
                     maior = cidade[i][j];
                }
            }
        }
        return maior;
    
}

/**
     * @param {number[][]} cidadezi
     */
function carro(cidadezi){
        let menor = 100
        
        for (let i = 0; i < cidadezi.length; i++) {
            for(let j = 0; j<cidadezi[i].length; j++){
                if(cidadezi[i][j] < menor && cidadezi[i][j] != 1 && cidadezi[i][j] != 0 ){
                    menor = cidadezi[i][j];
                }
            }
        }
        return menor;
        
}

rota(city)

</script>
<h1>em tese mapa do jogo</h1>
<a href="/">link pra voltar á home</a>
<h2>aqui em baixo array :V</h2>

<table class="haha">
    
    {#each city as linha,i}
    <tr> 
        {#each linha as _city,j}
            <td>{city[i][j]}</td>
        
        {/each}
    </tr>
    {/each}

</table>
<h2>era pra ser isso mas vai deixar de ser:</h2>
<p>  1 = pista 
    <br>
    maior numero = objetivo
    <br>
    0 = casas/coisas
    <br> 
    2(ou menor numero exceto por 1 e 0) = carro</p>

<style>
    table, td{
        border: 1px solid black;
        padding: 20px;
    }


</style>