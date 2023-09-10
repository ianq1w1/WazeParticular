<script lang="js">

    function findPath(matrix) {
      // Base case: If the current cell is out of bounds or already visited, return false.
     /* if (row < 0 || col < 0 || row >= matrix.length || col >= matrix[0].length || matrix[row][col] === 0) {
        return false;
      }*/
    
      var rua = CountRua(matrix);
      var carro = FoundCar(matrix);
      var destiny = FindDestiny(matrix);
    
      var RowCar = 0;
      var ColCar = 0;
    
      var RowDestiny = 0;
      var ColDestiny = 0;
    
    
    
      for(let i = 0; i < matrix.length; i++){
        for(let j = 0; j < matrix[i].length; j++){
            if(matrix[i][j] === carro){
                RowCar = i
                ColCar = j
            }
            if(matrix[i][j] === destiny){
                RowDestiny = i
                ColDestiny = j
            }
        }
      }
      
    
      // Base case: If the current cell is 2 (destination), we've found a path.
      /*if (matrix[row][col] === 2) {
        return true;
      }*/
    
      // Mark the current cell as visited.
      //matrix[row][col] = 0;
    
      // Recursively explore neighboring cells in all four directions.
     /* if (
        findPath(matrix, row - 1, col) ||
        findPath(matrix, row + 1, col) ||
        findPath(matrix, row, col - 1) ||
        findPath(matrix, row, col + 1)
      ) {
        return true;
      }*/
    //console.log(moveValido(matrix, RowCar - 1, ColCar) )
    
      for(let i = 0; i < matrix.length; i++ ){
        for(let j = 0; j < matrix[i].length + 1; j++){
            if (moveValido(matrix, i, j)){
                console.log(i,j)
                matrix[i][j] = 7
                return true;
            }if (moveValido(matrix, i, j)){
                console.log(i,j)
                matrix[i][j] = 7
                return true;
            }if (moveValido(matrix, i, j)){
                console.log(i,j)
                matrix[i][j] = 7
                return true;
            }if (moveValido(matrix, i, j)){
                console.log(i,j)
                matrix[i][j] = 7
                return true;
            }
        }
      }
    
      // If no path is found from this cell, backtrack and mark it as unvisited.
     /* matrix[row][col] = 1;
      return false;*/
    }
    
    // Given matrix
    let city = [
  [0, 0, 0, 0, 1, 1, 1, 0],
  [1, 1, 1, 1, 1, 0, 1, 0],
  [1, 0, 1, 0, 2, 0, 1, 0],
  [1, 0, 1, 0, 0, 0, 1, 0],
  [1, 0, 1, 0, 0, 0, 1, 0],
  [5, 1, 1, 1, 1, 1, 1, 0],
];
    
    
    function CountRua(matrix){
        var rua = 0;
        for(let i = 0; i < matrix.length; i++){
            for(let j = 0; j < matrix[i].length; j++){
                if(matrix[i][j] === 1){
                    rua = matrix[i][j] ;
                }
            }
        }
        return rua;
    }
    function FoundCar(matrix){
        var carrinho = 0;
        for(let i = 0; i < matrix.length; i++){
            for(let j = 0; j < matrix[i].length; j++){
                if(matrix[i][j] === 2){
                    carrinho = matrix[i][j] ;
                }
            }
        }
        return carrinho;
    }
    
    function FindDestiny(matrix){
        var destiny = 0;
        for(let i = 0; i < matrix.length; i++){
            for(let j = 0; j < matrix[i].length; j++){
                if(matrix[i][j] === 5){
                    destiny = matrix[i][j] ;
                }
            }
        }
        return destiny;
    }
    function moveValido(matrix, row, col){
        if(row < 0 || col < 0 || row >= matrix.length || col >= matrix[0].length || matrix[row][col] == 0 || matrix[row][col] == 2){
            return false;
        }else if (matrix[row][col] === 5){
            return true;
        }
      }
    // Find a path from 5 to 2 (start from row 1, column 6)
    const foundPath = findPath(city);
    
    if (foundPath) {
      console.log("Path found!");
    } else {
      console.log("Path not found.");
    }
    
    
    
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
                            <img src="src\images\pista.png" alt="pista">
                        </td>
                    {/if}
                    {#if city[i][j] == (7)}
                        <td>
                            <img src="src\images\relampago.png" alt="relampago">
                        </td>
                    {/if}
                {/each}
            </tr>
            {/each}
        </table>

        <div class="pastinha">
            <a href="/" class="casa">🏠 Você Chegou ao seu destino.</a>
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
        margin: 0 auto;
    }

    h2 {
        text-align: center;
        margin: 5px;
        color: rgb(26, 34, 58);
        font-size: 60px;
    }

    table {
        height: 15px;
        width: 15px; 
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

    .casa{
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