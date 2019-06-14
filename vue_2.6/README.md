本节代码对应课程2.6

使用component组件化思想修改todolist代码，总结如下：

1. 全局注册组件
    ```
    Vue.component('TodoItem',{
        prop: ['content'],
        template: '<li>{{content}}</li>'
    });
    ```

    在html中使用组件TodoItem
    ```
    <todo-item v-bind:content='item' v-for='item in list'></todo-item>
    ```

    组件中prop用于接收组件传递的值
    v-bind用于绑定html自定义属性
    注册的组件使用驼峰命名，组件的第二个大写字母在html中使用横线分隔符加小写

2. 局部注册组件
    ```
    var TodoItem = {
        prop: ['conten'],
        template: '<li>{{content}}</li>'
    };
    ```

    vue实例中注册TodoItem
    ```
    var app = new Vue({
        el: '#app',
        //局部注册组件
        components: {
            TodoItem: TodoItem
        },
        ...
    });
    ```

    在html中使用组件TodoItem
    ```
    <todo-item v-bind:content='item' v-for='item in list'></todo-item>
    ```



