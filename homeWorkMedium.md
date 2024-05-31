```java
package week9;
//When I started to try to make code nicer and trued to separate it in a different methods, the CODE DOES NOT WORK.
// I understand that probably the methods are taking or not giving the info from right places,
// but I don't know how to do it in a correct way.

import java.util.Scanner;

public class IndividTask1Copy {
    public static void main(String[] args) {

        int[][] grid = new int[3][3];
        Scanner sc = new Scanner(System.in);
        int turns = 9;
        // boolean gameWon = false;
        int player1InputRow = 0;
        int player1InputColumn = 0;
        int player1 = 1;
        int player2InputRow = 0;
        int player2InputColumn = 0;
        int player2 = 2;

        while (turns >= 0) {
            if (turns % 2 == 1) {
                System.out.println("Player 1 ");
                System.out.println("write a row number 1, 2 or 3: ");
                player1InputRow = sc.nextInt() - 1;
                System.out.println("write a column number 1, 2 or 3: ");
                player1InputColumn = sc.nextInt() - 1;

                for (int i = 0; i < grid.length; i++) {
                    for (int j = 0; j < grid[i].length; j++) {
                        if (grid[i][j] == grid[player1InputRow][player1InputColumn]) {
                            grid[player1InputRow][player1InputColumn] = player1;
                        }
                        System.out.print(grid[i][j] + " ");
                    }
                    System.out.println(" ");
                }
                if (grid[player1InputRow][0] == 1 && grid[player1InputRow][1] == 1 && grid[player1InputRow][2] == 1 ||
                        grid[0][player1InputColumn] == 1 && grid[1][player1InputColumn] == 1 && grid[2][player1InputColumn] == 1) {
                    System.out.print("Player" + player1 + ", Congratulations, you won!");
                    break;
                }
                turns = turns - 1;
            }
            if (turns % 2 == 0) {
                System.out.println("Player 2 ");
                System.out.println("write a row number 1, 2 or 3: ");
                player2InputRow = sc.nextInt() - 1;
                System.out.println("write a column number 1, 2 or 3: ");
                player2InputColumn = sc.nextInt() - 1;

                for (int i = 0; i < grid.length; i++) {
                    for (int j = 0; j < grid[i].length; j++) {
                        if (grid[i][j] == grid[player2InputRow][player2InputColumn]) {
                            grid[player2InputRow][player2InputColumn] = player2;
                        }
                        System.out.print(grid[i][j] + " ");
                    }
                    System.out.println(" ");
                }
                if (grid[player2InputRow][0] == 2 && grid[player2InputRow][1] == 2 && grid[player2InputRow][2] == 2 ||
                        grid[0][player2InputColumn] == 2 && grid[1][player2InputColumn] == 2 && grid[2][player2InputColumn] == 2) {
                    System.out.println("Player " + player2 + ", you won!!!");
                    break;
                }
                turns = turns - 1;
            }
        }
    }
}
 /*   public static void chooseRowAndColumn(int row, int column, Scanner sc, int[][] grid, int player) {
        System.out.println("write a row number 1, 2 or 3: ");
        row = sc.nextInt() - 1;
        System.out.println("write a column number 1, 2 or 3: ");
        column = sc.nextInt() - 1;

        for (int i = 0; i < grid.length; i++) {
            for (int j = 0; j < grid[i].length; j++) {
                if (grid[i][j] == grid[row][column]) {
                    grid[row][column] = player;
                }
                System.out.print(grid[i][j] + " ");
            }
            System.out.println(" ");
        }
    }


   /* public static boolean winCondition(int row, int column, int[][] grid, int player) {
        if (grid[row][0] == player && grid[row][1] == player && grid[row][2] == player || grid[0][column] == player && grid[1][column] == player && grid[2][column] == player) {
            return true;
        }
        return false;
    }

    public static void fillIn(int row, int column, int player, int[][] grid) {
        for (int i = 0; i < grid.length; i++) {
            for (int j = 0; j < grid[i].length; j++) {
                if (grid[i][j] == grid[row][column]) {
                    grid[row][column] = player;
                }
                System.out.print(grid[i][j] + " ");
            }
            System.out.println(" ");
        }

    */
```
