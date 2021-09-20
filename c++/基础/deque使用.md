# deque 使用
## deque函数
+ deque 容器为一个给定类型的元素进行线性处理，像向量一样，它能够快速地随机访问一个元素，并且能够高效地
    插入和删除容器尾部元素，但它与 vector 不同，deque 支持高效插入和删除容器的头部元素，因此也叫做双端
    队列，

    * 1. 构造函数
        > deque() 创建一个空 deque
        > deque(int nSize): 创建一个deque，元素个数为 nSize
        > deque(int nSize, const T& t):创建一个deque，元素为 nSize ，且均值为 t
        > deque(const deque&):复制构造函数

    * 2. 增加函数
        > void push_fron(const T& x): 双端队列头部增加一个元素X
        > void push_back(const T& x): 双端队列尾部增加一个元素X
        > iterator insert(iterator it,const T& x): 双端队列中某一个元素前增加一个元素X
        > void insert(iterator it, int n, const T& x):双端队列中某一元素前增加 n个 相同的元素 X
        > void insert(iterator it,const_iterator first, const_iterator last): 双端队列中某一元素前插入另一个相同类型向量的[first,last]间的数据

    * 3. 删除数据
        > iterator erase(iterator it):删除双端队列中的某一个元素
        > iterator erase(iterator first, iterator last) 删除双端队列中 [first, last] 中的元素
        > void pop_front():删除双端队列中最前一个元素
        > void pop_back():删除双端队列中最后一个元素
        > void clear(): 清空双端队列中最后一个元素

    * 4. 遍历函数
        > referenct at(int pos):返回pos位置元素的索引
        > referenct font(): 返回首元素的引用
        > referenct back(): 返回尾元素的引用
        > iterator begin(): 返回向量头指针，指向的第一个元素
        > iterator end(): 返回指向向量中最后一个元素下一个元素的指针（不包含在向量中）
        > reverse_iterator rbegin(): 反向迭代器，指向最后一个元素
        > reverse_iterator rend(): 反向迭代器，指向第一个元素的前一个元素

    * 5. 判断函数
        > empty(): const：向量是否为空，若 true 则向量中无元素

    * 6. 大小函数
        > int size() const: 返回向量中元素的个数
        > int max_size() const: 返回最大可允许的双端队列元素数量值

    * 7. 其他函数
        > void swap(deque&): 交换两个同类型向量的数据
        > void assign(int n, const T& x): 向量中第 n 个元素的值设置为 x
