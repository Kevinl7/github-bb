
#  什么是数据结构？
 >  数据结构是在计算机中组织和存储数据的一种特殊方式，使得数据可以高效地被访问和修改。更确切地说，数据结构是数据值的集合，表示数据之间的关系，也包括了作用在数据上的函数或操作。

***
-  八大常见的数据结构
  * 数组：Array
  * 堆栈：Stack
  * 队列：Queue
  * 链表：Linked Lists
  * 树：Trees
  * 图：Graphs
  * 字典树：Trie
  * 散列表（哈希表）：Hash Tables

 > 在较高的层次上，基本上有三种类型的数据结构:

  * 堆栈和队列是类似于数组的结构，仅在项目的插入和删除方式上有所不同。
  * 链表，树，和图 结构的节点是引用到其他节点。
  * 散列表依赖于散列函数来保存和定位数据。

> 在复杂性方面：

  * 堆栈和队列是最简单的，并且可以从中构建链表。
  * 树和图 是最复杂的，因为它们扩展了链表的概念。
  * 散列表和字典树 需要利用这些数据结构来可靠地执行。


> 就效率而已：

  * 链表是记录和存储数据的最佳选择
  * 而哈希表和字典树 在搜索和检索数据方面效果最佳。
  
***

### 堆栈： Stack

> 堆栈是元素的集合，可以在顶部添加项目, 两个原则操作：push和pop。Push 将元素添加到数组的顶部，而Pop将它们从同一位置删除, 遵循"Last In，First Out"，即：LIFO，后进先出。

```
  class Stack {
    constructor(...items) {
      this.reverse = false
      this.stack = [...items]
    }

    push(...items) {
      return this.reverse
        ? this.stack.unshift(...items)
        : this.stack.push(...items)
    }

    pop() {
      return this.reverse ? this.stack.shift() : this.stack.pop()
    }
  }
  const stack = new Stack(4, 5)
  stack.reverse = true
  console.log(stack.push(1, 2, 3) === 5) // true
  console.log(stack.stack ===[1, 2, 3, 4, 5]) // true

```

### 队列： Queue
> 在计算机科学中，一个队列(queue)是一种特殊类型的抽象数据类型或集合。集合中的实体按顺序保存。在前端开发中，最著名的队列使用当属浏览器/NodeJs中 关于宏任务与微任务，任务队列. 遵循"Fist In，first out"即：FIFO，先进先出。

```
class Queue {
  constructor(...items) {
    this.reverse = false
    this.queue = [...items]
  }

  enqueue(...items) {
    return this.reverse
      ? this.queue.push(...items)
      : this.queue.unshift(...items)
  }

  dequeue() {
    return this.reverse ? this.queue.shift() : this.queue.pop()
  }
}


```












