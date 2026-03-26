任务描述  
编程要求  
测试说明  
任务描述  
本关任务：在n×n格的棋盘上放置彼此不受攻击的n个皇后。按照国际象棋的规则，皇后可以攻击与之处在同一行或同一列或同一斜线上的棋子。用递归算法解决该问题。

编程要求  
请在右侧编辑器Begin-End处补充代码，完成本关任务。

测试说明  
平台会对你编写的代码进行测试，比对你输出的数值与实际正确数值，只有所有数据全部计算正确才能通过测试：

测试输入：4（皇后的数目）

预期输出：

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/080e89d89c9148f985e090c249dd4977.png)

4后问题共有2种摆放方案  
开始你的任务吧，祝你成功！

```
package step2;
import java.util.ArrayList;
import java.util.List;
import java.util.Scanner;
public class Nqueens{
      private int[] queens; // 用于存储每一行皇后的列位置
    private List<int[]> solutions; // 用于存储所有解决方案

    public Nqueens(int n) {
        queens = new int[n]; // 初始化皇后数组，长度为n
        solutions = new ArrayList<>(); // 初始化解决方案列表
    }

    public void solve() {
        solve(0); // 从第0行开始解决N皇后问题
    }

    private void solve(int row) {
        if (row == queens.length) {
            // 如果已经处理完所有行，说明找到了一个解决方案
            solutions.add(queens.clone()); // 将当前的皇后位置数组添加到解决方案列表中
            return;
        }

        for (int col = 0; col < queens.length; col++) {
            if (isSafe(row, col)) {
                // 如果当前位置是安全的，放置皇后
                queens[row] = col;
                solve(row + 1); // 递归处理下一行
                queens[row] = -1; // 回溯，移除当前行的皇后
            }
        }
    }

    private boolean isSafe(int row, int col) {
        for (int i = 0; i < row; i++) {
            // 检查当前位置是否与之前的皇后位置冲突
            if (queens[i] == col ||
                    queens[i] - i == col - row ||
                    queens[i] + i == col + row) {
                return false; // 如果有冲突，返回false
            }
        }
        return true; // 如果没有冲突，返回true
    }

    public void printSolutions() {
        // 打印所有解决方案
        for (int[] solution : solutions) {
            for (int i = 0; i < solution.length; i++) {
                System.out.print("  "); // 打印前导空格
                for (int j = 0; j < solution.length; j++) {
                    if (solution[i] == j) {
                        System.out.print("Q"); // 打印皇后
                    } else {
                        System.out.print("*"); // 打印空位
                    }
                    if (j < solution.length - 1) {
                        System.out.print("  "); // 打印列之间的空格
                    }
                }
                System.out.println(); // 换行
            }
            System.out.println(); // 打印解决方案之间的空行
        }
        System.out.println(queens.length + "后问题共有" + solutions.size() + "种摆放方案"); // 打印总的解决方案数量
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        // 从用户输入中获取N的值
        int n = scanner.nextInt();
        scanner.close();

        Nqueens nQueens = new Nqueens(n); // 创建N皇后问题的实例
        nQueens.solve(); // 解决N皇后问题
        nQueens.printSolutions(); // 打印所有解决方案
    }
}

```