本节代码对应课程3.7 （条件渲染）  总结如下：

1. v-if的值为false，整个元素将被移除，v-show的值为false，隐藏该元素。从性能上来看，v-show性能更好
2. v-if扩展用法：

    1. 使用key区分相同标签
    ```
    <div v-if='show === "a"'>
        用户名：<input type="text" key="username">
    </div>
    <div v-else>
        密码：<input type="text" key="password">
    </div>
    ```
    2. 模板中使用if, else if, else
    ```
    <div v-if='show === "a"'>
        this is a
    </div>
    <div v-else-if='show === "b"'>
        this is b
    </div>
    <div v-else>
        other thing
    </div>
    ```


