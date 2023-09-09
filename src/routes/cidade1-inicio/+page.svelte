<script>
    let city = [
  [0, 0, 0, 0, 0, 0, 0, 0],
  [0, 0, 1, 1, 1, 1, 5, 0],
  [1, 1, 1, 0, 0, 0, 1, 0],
  [0, 0, 1, 0, 0, 0, 1, 0],
  [0, 0, 1, 0, 0, 0, 1, 0],
  [0, 0, 2, 1, 1, 1, 1, 0],
];

</script>

<body>
    <div class="content">
        <h2>Mapa</h2>

        <table>
            {#each city as linha, i}
            <tr>
                {#each linha as _city, j}
                    {#if city[i][j] == (0)}
                        <td>
                            <img src="src\images\casa.png" alt="casa">
                        </td>
                    {/if}
                    {#if city[i][j] == (1)}
                        <td>
                            <img src="src\images\pista.png" alt="pista">
                        </td>
                    {/if}
                    {#if city[i][j] == (2)}
                        <td>
                            <img src="src\images\relampago.png" alt="relampago">
                        </td>
                    {/if}
                    {#if city[i][j] == (5)}
                        <td>
                            <img src="src\images\ifpe.png" alt="if">
                        </td>
                    {/if}
                {/each}
            </tr>
            {/each}
        </table>

        <div class="pastinha">
            <a href="/" class="casa">🏠 Home</a>
            <a href="/cidade1-final" class="btnRota">🚶‍♂️ Faça a rota</a>
        </div>
    </div>
</body>

<style>
    body {
        display: flex;
        justify-content: center;
        align-items: center;
        min-height: 100vh;
        margin: 0;
    }

    .content {
        text-align: center;
        margin: 0 auto;}

    h2 {
        text-align: center;
        margin: 5px;
        color: rgb(26, 34, 58);
        font-size: 60px;
    }

    table {
        border-collapse: collapse; 
    }

    tr, td {
        padding: 0px;
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
