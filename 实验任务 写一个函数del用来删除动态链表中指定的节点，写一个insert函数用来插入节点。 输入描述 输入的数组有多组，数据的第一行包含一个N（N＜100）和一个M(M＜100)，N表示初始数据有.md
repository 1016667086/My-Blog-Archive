实验任务  
写一个函数del用来删除动态链表中指定的节点，写一个insert函数用来插入节点。

输入描述  
输入的数组有多组，数据的第一行包含一个N（N<100）和一个M(M<100)，N表示初始数据有N个，接下来输入N个数据，M表示有多少条删除或插入的语句。如“D 1”表示删除第一个节点，“I 100 3”表示将100插入到第三个位置。

输出描述  
输出最后的结果。

输入样例  
3 4

11 22 33

D 3

D 2

I 100 1

I 200 2

输出样例  
100 200 11

提示

题目来源  
谭浩强《C程序设计（第五版）》例9.8-9.9

内存限制:128mb 时间限制:1000ms  
开始你的实验吧，祝你成功！

```
#include <stdio.h>
#include <stdlib.h>

typedef struct Node {
    int data;
    struct Node *next;
} Node;

Node* createList(int arr[], int n) {
    Node *head = NULL, *tail = NULL;
    for (int i = 0; i < n; i++) {
        Node *newNode = (Node*)malloc(sizeof(Node));
        newNode->data = arr[i];
        newNode->next = NULL;
        if (head == NULL) {
            head = tail = newNode;
        } else {
            tail->next = newNode;
            tail = newNode;
        }
    }
    return head;
}

Node* del(Node *head, int pos) {
    if (head == NULL || pos < 1) return head;
    if (pos == 1) {
        Node *temp = head;
        head = head->next;
        free(temp);
        return head;
    }
    Node *current = head;
    int count = 1;
    while (current != NULL && count < pos - 1) {
        current = current->next;
        count++;
    }
    if (current == NULL || current->next == NULL) return head;
    Node *temp = current->next;
    current->next = temp->next;
    free(temp);
    return head;
}

Node* insert(Node *head, int value, int pos) {
    if (pos < 1) return head;
    Node *newNode = (Node*)malloc(sizeof(Node));
    newNode->data = value;
    newNode->next = NULL;
    if (pos == 1) {
        newNode->next = head;
        return newNode;
    }
    Node *current = head;
    int count = 1;
    while (current != NULL && count < pos - 1) {
        current = current->next;
        count++;
    }
    if (current == NULL) {
        free(newNode);
        return head;
    }
    newNode->next = current->next;
    current->next = newNode;
    return head;
}

void printList(Node *head) {
    Node *current = head;
    while (current != NULL) {
        printf("%d", current->data);
        if (current->next != NULL) printf(" ");
        current = current->next;
    }
    printf("\n");
}

void freeList(Node *head) {
    Node *temp;
    while (head != NULL) {
        temp = head;
        head = head->next;
        free(temp);
    }
}

int main() {
    int N, M;
    while (scanf("%d %d", &N, &M) != EOF) {
        int arr[100];
        for (int i = 0; i < N; i++) {
            scanf("%d", &arr[i]);
        }
        Node *head = createList(arr, N);
        for (int i = 0; i < M; i++) {
            char cmd;
            scanf(" %c", &cmd);
            if (cmd == 'D') {
                int pos;
                scanf("%d", &pos);
                head = del(head, pos);
            } else if (cmd == 'I') {
                int value, pos;
                scanf("%d %d", &value, &pos);
                head = insert(head, value, pos);
            }
        }
        printList(head);
        freeList(head);
    }
    return 0;
}

```

**代码解释：**

1. **链表结构体定义**：使用`Node`结构体表示链表节点，包含数据和指向下一个节点的指针。
2. **创建链表函数**：根据输入的数组构建链表，返回头指针。
3. **删除节点函数**：处理删除指定位置的节点，考虑头节点和其他位置的删除，确保链表正确连接。
4. **插入节点函数**：在指定位置插入新节点，处理头部插入和中间/尾部插入的情况。
5. **输出链表函数**：遍历链表并按格式输出数据。
6. **主函数**：读取输入数据，创建初始链表，处理所有操作命令，最后输出结果并释放内存。

**关键点处理：**

* **输入处理**：使用循环读取多组输入，直到文件结束。
* **命令解析**：根据命令类型调用对应的删除或插入函数。
* **内存管理**：在程序结束前释放链表占用的内存，避免内存泄漏。

此代码能够正确应对题目中的各种情况，包括删除和插入操作的位置合法性检查，并确保最终链表正确输出。