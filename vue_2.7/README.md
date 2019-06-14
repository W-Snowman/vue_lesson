本节代码对应课程2.7

进一步学习component组件之间传值，总结如下：

- 子组件向父组件传值
    1. 子组件中绑定事件，触发事件时使用$emit来触发自定义事件，并传递参数
    ```
    //局部注册组件(子组件)
    var TodoItem = {
        props: ['content','index'],
        template: '<li @click="deleteItem">{{content}}</li>',
        methods:{
            deleteItem: function(){
                this.$emit('click',this.index);
            }
        }
    };
    ```
    2. 父组件中使用子组件，监听该自定义事件
    ```
    <todo-item  :content="item"
                :index="index" 
                v-for="(item,index) in list"
                @click="clickItem">
    </todo-item>
    ```
    3. 在vue实例中写该方法需要处理的事情
    ```
    var app = new Vue({
        el: '#app',
        //局部注册组件
        components: {
            TodoItem: TodoItem
        },
        data: {
            list: [],
            todo: ''
        },
        methods: {
            submit: function() {
                this.list.push(this.todo);
                this.todo = '';
            },
            clickItem: function(data){
                this.list.splice(data,1);
            }
        }
    })
    ```



