<script lang='js'>




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
    console.log(parada)
    
    /*for(i = i; i >= rua; i--){
        for(j = j; j>=rua; j--){
            if(parada >= rua){
                console.log(route[i][j]) 
            }
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
                    return maior = cidade[i][j];
                }
            }
        }
        return maior;
    
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
    5 = objetivo
    <br>
    0 = casas
    <br> 
    2 = carro</p>