<script lang="js">




    export let city = [
        [1,1,1,7,1,1,0],
        [1,0,0,1,0,1,0],
        [1,0,0,1,0,1,0],
        [1,0,0,1,1,1,0],
        [1,1,0,1,0,0,0],
        [0,1,1,2,0,0,0],
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
    var yparada = 0

    // FUNÇÃO localização linha e coluna do carro 
    for(xcarro = 0; xcarro<route.length; xcarro++){
        for(ycarro = 0; ycarro<route[xcarro].length; ycarro++){
            if(route[xcarro][ycarro] == partida){
                xcarro = xcarro;
                ycarro = ycarro;
            }  
        }
    }
    // FUNÇÃO localização linha e coluna do objetivo/parada    
    for(xparada = 0; xparada<route.length; xparada++){
        for(yparada = 0; yparada<route[xparada].length; yparada++){
            if(route[xparada][yparada] == parada){
                xparada = xparada;
                yparada = yparada;
            }
        }
    }


    //FUNÇÃO REALOCAR POSIÇÃO DO CARRO 

  /*  for(route[xcarro] != route[xparada]; route[xcarro] <= route[xparada]; xcarro++){
        for(route[ycarro] != route[yparada]; route[ycarro] <= route[yparada]; ycarro++){
            if(route[xcarro][ycarro] <)
        }
    }*/

    
}

// pega o maior numero da array (objetivo)
/**
     * @param {number[][]} cidade
     */
function maiorNum(cidade){
    let maior = cidade[0][0]; 

    for (let i = 0; i < cidade.length; i++) {
            for(let j = 0; j<cidade[i].length+1; j++){
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

<table>
    
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