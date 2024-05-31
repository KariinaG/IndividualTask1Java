```java
//EASY
import java.util.Scanner;

public class IndividualTask1 {
    public static void main(String[] args) {

        int[][] grid = new int[3][3];
        Scanner sc = new Scanner(System.in);
        int turns = 9;

        while (turns > 0) {
            System.out.println("write a row number 1, 2 or 3: ");
            int player1InputRow = sc.nextInt() - 1;
            System.out.println("write a column number 1, 2 or 3: ");
            int player1InputColumn = sc.nextInt() - 1;

            for (int i = 0; i < grid.length; i++) {
                for (int j = 0; j < grid[i].length; j++) {
                    if (grid[i][j] == grid[player1InputRow][player1InputColumn]) {
                        grid[player1InputRow][player1InputColumn] = 1;
                        // System.out.print(grid[i][j] + " ");
                    }
                    System.out.print(grid[i][j] + " ");
                }
                System.out.println();
            }
            turns--;
            if (grid[player1InputRow][0] == 1 && grid[player1InputRow][1] == 1 && grid[player1InputRow][2] == 1 ||
                    grid[0][player1InputColumn] == 1 && grid[1][player1InputColumn] == 1 && grid[2][player1InputColumn] == 1) {
                System.out.print("you won!");
                break;
            }
        }
        sc.close();
    }
}
```
