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
        maior numero = objetivo, se ele se tornou um 7 quer dizer q ele chegou no objetivo
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