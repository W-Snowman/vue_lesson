本节代码对应课程3.1-3.4 （主要代码是3.4）  总结如下：

- 3.2小节主要讲vue实例与生命周期函数，理解生命周期函数的定义，以及各个函数触发的时间节点
- 3.3小节主要讲模板语法，常用有：
    1. 插值表达式
    ```
    <div>{{ msg }}</div>
    <div>{{ msg + '123'}}</div>  //插值表达式支持完整的js表达式
    ```
    2. v-text (等同于插值表达式)
    3. v-html (可渲染带有标签的data)
    4. v-bind   绑定html标签属性
    ```
    <div v-bind:class="num"></div>
    <div :class="num"></div>    //简写
    ```
    5. v-model  (数据双向绑定)
    ```
    <input type="text" v-model="msg">
    ```
    6. v-on (事件)
    ```
    <button v-on:click="handle"></button>
    <button @click="handle"></button>
    ```
    7. v-if
    ```
    <div v-if="seen">显示</div>
    ```
    8. v-for
    ```
    <ul>
        <li v-for"(item, index) in list"></li>
    </ul>
    ```
- 3.4小节主要讲计算属性与侦听器 
    计算等逻辑代码不应放入模板语法中，使代码的可读性变差，应使用计算属性代替，详见index.html代码
    计算属性带有缓存
    



