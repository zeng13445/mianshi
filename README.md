# 记录一下面试的笔记
- java
1. HashMap：
    - 阐述
    ```
    底层主要是基于数组外加链表组成，链表主要是为了解决hash冲突。
    ```
    - 默认容量和扩容机制
    ```
    默认capacity 16，默认负载因子0.75，所有当大于12时才发生扩容（一倍）。扩容是很消耗性能的，所以最好提前预估初始大小以减少扩容带来的性能损耗。
    ```
    - put、get（1.8）
    ```
    根据key计算出hashcode，然后定位出所在的桶（当前位置），再将value放入。get类似，也是通过key算出hashcode，再定位到桶，取值。
    ```
     ![image](https://github.com/zeng13445/mianshi/blob/main/images/put.png)
    - 初始化
    ```
    若在构造函数中指定了容量大小7，那么该容量其实是8，因为hash会选择大于该数字的第一个2的n次幂作为容量（即3->4、7->8、9->16）。
    ```
    
