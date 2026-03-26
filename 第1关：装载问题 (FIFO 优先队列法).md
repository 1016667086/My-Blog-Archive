问题描述  
任务描述  
相关知识  
算法改进  
构造最优解  
编程要求  
测试说明  
问题描述  
有一批共个集装箱要装上 2 艘载重量分别为 C1 和 C2 的轮船，其中集  
装箱 i 的重量为 Wi ，且  
装载问题要求确定是否有一个合理的装载方案可将这个集装箱装上这2艘轮船。如果有，找出一种装载方案。

容易证明：如果一个给定装载问题有解，则采用下面的策略可得到最优装载方案。

(1)首先将第一艘轮船尽可能装满；

(2)将剩余的集装箱装上第二艘轮船。

任务描述  
本关任务：采用队列式分支限界法来完成装载问题

相关知识  
在算法的 while 循环中，首先检测当前扩展结点的左儿子结点是否为可行结点。如果是则将其加入到活结点队列中。然后将其右儿子结点加入到活结点队列中(右儿子结点一定是可行结点)。 2 个儿子结点都产生后，当前扩展结点被舍弃。  
活结点队列中的队首元素被取出作为当前扩展结点，由于队列中每一层结点之后都有一个尾部标记 -1 ，故在取队首元素时，活结点队列一定不空。当取出的元素是 -1 时，再判断当前队列是否为空。如果队列非空，则将尾部标记 -1 加入活结点队列，算法开始处理下一层的活结点。

while (true) {  
// 检查左儿子结点  
if (Ew + w[i] <= c) // x[i] = 1  
EnQueue(Q, Ew + w[i], bestw, i, n);  
// 右儿子结点总是可行的  
EnQueue(Q, Ew, bestw, i, n); // x[i] = 0  
Q.Delete(Ew); // 取下一扩展结点  
if (Ew == -1) { // 同层结点尾部  
if (Q.IsEmpty()) return bestw;  
Q.Add(-1); // 同层结点尾部标志  
Q.Delete(Ew); // 取下一扩展结点  
i++;} // 进入下一层 } }

算法改进  
节点的左子树表示将此集装箱装上船，右子树表示不将此集装箱装上船。设 bestw 是当前最优解； ew 是当前扩展结点所相应的重量； r 是剩余集装箱的重量。则当 ew+rbestw 时，可将其右子树剪去，因为此时若要船装最多集装箱，就应该把此箱装上船。

另外，为了确保右子树成功剪枝，应该在算法每一次进入左子树的时候更新 bestw 的值。

// 检查左儿子结点  
Type wt = Ew + w[i]; // 左儿子结点的重量  
if (wt <= c) { // 可行结点  
if (wt > bestw) bestw = wt;  
// 加入活结点队列  
if (i < n) Q.Add(wt);  
//检查右儿子结点  
if (Ew + r > bestw && i < n)  
Q.Add(Ew); // 可能含最优解  
Q.Delete(Ew); // 取下一扩展结点

构造最优解  
为了在算法结束后能方便地构造出与最优值相应的最优解，算法必须存储相应子集树中从活结点到根结点的路径。为此目的，可在每个结点处设置指向其父结点的指针，并设置左、右儿子标志。

class QNode  
{QNode \*parent; // 指向父结点的指针  
bool LChild; // 左儿子标志  
Type weight; // 结点所相应的载重量

编程要求  
请仔细阅读右侧代码，结合相关知识，在 Begin - End 区域内进行代码补充，完成使用队列式分支限界法来完成装载问题的任务

测试说明  
平台会对你编写的代码进行测试：

测试输入：  
4  
70  
20 10 26 15

预期输出：  
Ship load:70  
The weight of the goods to be loaded is:  
20 10 26 15  
Result:  
1 0 1 1  
The optimal loading weight is:61

开始你的任务吧，祝你成功！

```
package step1;
import java.util.*;

// 表示子集树中的节点
class BBNode {
    BBNode parent; // 指向父节点的指针
    boolean LChild; // 左儿子节点标识

    public BBNode(BBNode parent, boolean LChild) {
        this.parent = parent;
        this.LChild = LChild;
    }
}

// 表示优先队列中的节点
class HeapNode implements Comparable<HeapNode> {
    BBNode ptr; // 指向活节点在子集树中相应节点的指针
    double uweight; // 活节点优先级(上界)
    int level; // 活节点在子集树中所处的层序号

    public HeapNode(BBNode ptr, double uweight, int level) {
        this.ptr = ptr;
        this.uweight = uweight;
        this.level = level;
    }

    @Override
    public int compareTo(HeapNode other) {
        return Double.compare(other.uweight, this.uweight); // 最大堆
    }
}

public class MaxLoading {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int N = scanner.nextInt(); // 输入集装箱数量
        int c = scanner.nextInt(); // 输入第一艘轮船的载重量
        int[] w = new int[N + 1]; // 集装箱重量数组，下标从1开始
        for (int i = 1; i <= N; i++) {
            w[i] = scanner.nextInt(); // 输入每个集装箱的重量
        }

        System.out.println("Ship load:" + c); // 输出轮船载重量
        System.out.println("The weight of the goods to be loaded is:");
        for (int i = 1; i <= N; i++) {
            System.out.print(w[i] + " "); // 输出每个集装箱的重量
        }
        System.out.println();

        int[] bestx = new int[N + 1]; // 最优解数组，记录每个集装箱是否装载
        int bestw = maxLoading(w, c, N, bestx); // 调用maxLoading方法求解最优装载

        System.out.println("Result:");
        for (int i = 1; i <= N; i++) {
            System.out.print(bestx[i] + " "); // 输出最优解
        }
        System.out.println("\nThe optimal loading weight is:" + bestw); // 输出最优装载重量
    }

    // 将活节点加入到表示活节点优先队列的最大堆H中
    private static void addLiveNode(PriorityQueue<HeapNode> H, BBNode E, double wt, boolean ch, int lev) {
        BBNode b = new BBNode(E, ch); // 创建新的BBNode节点
        HeapNode N = new HeapNode(b, wt, lev); // 创建新的HeapNode节点
        H.add(N); // 将HeapNode节点加入优先队列
    }

    // 优先队列式分支限界法，返回最优载重量，bestx返回最优解
    private static int maxLoading(int[] w, int c, int n, int[] bestx) {
        PriorityQueue<HeapNode> H = new PriorityQueue<>(); // 创建优先队列
        double[] r = new double[n + 1]; // 剩余容量数组
        r[n] = 0; // 最后一个集装箱的剩余容量为0
        for (int j = n - 1; j > 0; j--) {
            r[j] = r[j + 1] + w[j + 1]; // 计算每个集装箱的剩余容量
        }

        int i = 1; // 当前扩展节点所处的层
        BBNode E = null; // 当前扩展节点
        double Ew = 0; // 当前扩展节点的载重量

        while (i != n + 1) { // 非叶子节点
            if (Ew + w[i] <= c) { // 检查左儿子节点
                addLiveNode(H, E, Ew + w[i] + r[i], true, i + 1); // 加入左儿子节点
            }
            // 右儿子节点总是可行的
            addLiveNode(H, E, Ew + r[i], false, i + 1); // 加入右儿子节点

            HeapNode N = H.poll(); // 取下一个扩展节点
            i = N.level; // 更新当前层
            E = N.ptr; // 更新当前扩展节点
            Ew = N.uweight - r[i - 1]; // 更新当前扩展节点的载重量
        }

        // 构造最优解
        for (int j = n; j > 0; j--) {
            bestx[j] = E.LChild ? 1 : 0; // 根据LChild标识确定是否装载
            E = E.parent; // 回溯到父节点
        }

        return (int) Ew; // 返回最优装载重量
    }
}

```