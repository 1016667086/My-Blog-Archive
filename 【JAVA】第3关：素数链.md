任务描述  
编程要求  
测试说明  
任务描述  
本关任务：把从 1 到 n 这 n 个数摆成一个链，要求相邻的两个数的和是一个素数。

编程要求  
请在右侧编辑器Begin-End处补充代码，完成本关任务，输出格式请参考测试集。

测试说明  
平台会对你编写的代码进行测试，比对你输出的数值与实际正确数值，只有所有数据全部计算正确才能通过测试：

测试输入：15  
预期输出：摆成的链是: 15 14 9 10 13 6 11 12 7 4 3 8 5 2 1

开始你的任务吧，祝你成功！

```
package step3;


import java.util.ArrayList;
import java.util.List;
import java.util.Scanner;

public class Prime {
    // 判断一个数是否为素数
    private static boolean isPrime(int num) {
        
        if (num < 2) {
            return false; // 小于2的数不是素数
        }
        for (int i = 2; i * i <= num; i++) {
            if (num % i == 0) {
                return false; // 如果能被整除，则不是素数
            }
        }
        return true; // 否则是素数
    }

    // 判断两个数是否可以相连（即它们的和是否为素数）
    private static boolean canLink(int a, int b) {
        return isPrime(a + b); // 返回两个数之和是否为素数
    }

    // 寻找一个长度为n的链，链中的每两个相邻元素的和都是素数
    private static List<Integer> findChain(int n) {
        List<Integer> result = new ArrayList<>(); // 存储结果链
        boolean[] used = new boolean[n + 1]; // 标记数组，记录哪些数已经被使用

        // 从n开始向下寻找第一个未使用的数，并将其加入链中
        for (int i = n; i >= 1; i--) {
            if (!used[i]) {
                result.add(i); // 将未使用的数加入链中
                used[i] = true; // 标记该数为已使用
                break; // 跳出循环
            }
        }

        // 继续寻找链中的下一个数，直到链的长度达到n
        while (result.size() < n) {
            int last = result.get(result.size() - 1); // 获取链中的最后一个数
            boolean found = false; // 标记是否找到下一个数
            for (int next = n; next >= 1; next--) {
                if (!used[next] && canLink(last, next)) {
                    // 如果找到一个未使用且可以与最后一个数相连的数，将其加入链中
                    result.add(next);
                    used[next] = true; // 标记该数为已使用
                    found = true; // 标记找到下一个数
                    break; // 跳出循环
                }
            }
            if (!found) {
                // 如果没有找到下一个数，返回空链
                return new ArrayList<>();
            }
        }
        return result; // 返回找到的链
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in); // 创建Scanner对象用于读取用户输入
        int n = scanner.nextInt(); // 从用户输入中获取n的值
        List<Integer> chain = findChain(n); // 寻找长度为n的链

        System.out.print("摆成的链是: "); // 打印提示信息
        for (int num : chain) {
            System.out.print(num + " "); // 打印链中的每个数
        }
        System.out.println(); // 换行
        scanner.close(); // 关闭Scanner
    }
}

```