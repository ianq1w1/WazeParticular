<script>
    let city = [
  [0, 0, 0, 0, 1, 1, 5, 0],
  [1, 1, 1, 1, 1, 0, 1, 0],
  [1, 0, 0, 0, 0, 0, 1, 0],
  [1, 1, 1, 0, 0, 0, 1, 0],
  [0, 0, 1, 0, 0, 0, 1, 0],
  [0, 0, 2, 1, 1, 1, 1, 0],
];

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
<a href="/cidade2-final">
    <button class="">veja como ficará nessa rota :D</button>
</a>
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
