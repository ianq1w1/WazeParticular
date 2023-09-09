<script>
    let city = [
  [0, 0, 0, 0, 0, 0, 0, 0],
  [0, 0, 1, 1, 1, 1, 5, 0],
  [0, 0, 1, 0, 0, 0, 1, 0],
  [0, 0, 1, 0, 0, 0, 1, 0],
  [0, 0, 1, 0, 0, 0, 1, 0],
  [0, 0, 2, 1, 1, 1, 1, 0],
];

</script>

<h2>Mapa</h2>

<table>
    {#each city as linha, i}
    <tr>
        {#each linha as _city, j}
            <td class={"valor-" + city[i][j]}>{city[i][j]}</td>
        {/each}
    </tr>
    {/each}
</table>

<div class="pastinha">
    <a href="/" class="casa">🏠 Home</a>
    <a href="/cidade1-final" class="btnRota">🚶‍♂️ Faça a rota</a>
</div>

<!-- 
<div>
    <h2>era pra ser isso mas vai deixar de ser:</h2>
        1 = pista 
        <br>
        maior numero = objetivo
        <br>
        0 = casas/coisas
        <br> 
        2(ou menor numero exceto por 1 e 0) = carro
</div>
-->

<style>
    h2 {
        text-align: center;
        margin: 5px;
        color: rgb(26, 34, 58);
        font-size: 60px;
    }

    table {
        height: 15px;
        width: 15px;; 
    }

    .valor-0, .valor-1, .valor-2, .valor-5 {
        color: transparent;
    }

    .valor-0 {
        background-color: white;
    }

    .valor-1 {
        background-color: gray;
    }

    .valor-2 {
        background-color: red;
    }

    .valor-5 {
        background-color: green;
    }

    table {
        border-collapse: collapse; 
    }

    tr, td {
        padding: 30px;
        height: 20px;
        border: 1px solid #333; 
    }

    .pastinha a{
        display: inline-block;
        margin-right: 10px;
    }

    .btnRota, .casa{
        display: block;
        background: #5776cc;
        color: white;
        margin: 10px auto;
        padding: 10px 30px;
        border: none;
        border-radius: 5px;
        font-size: 18px;
        cursor: pointer;
        text-decoration: none;
    }
</style>
