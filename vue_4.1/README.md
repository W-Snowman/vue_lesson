本节代码对应课程4.1 （组件细节）  总结如下：

1. is属性的使用

    在某些特定的html下必须使用特定的标签，如<tbody>标签下面必须是<tr>标签，那么在使用组件的时候需要加上is属性来让浏览器识别这些标签:
    ```
    <!-- html -->
    <div id="app">
        <table>
            <tbody>
                <tr is='rows'></tr>
                <tr is='rows'></tr>
                <tr is='rows'></tr>
            </tbody>
        </table>
    </div>

    <!-- js -->
    <script>
        Vue.component('rows',{
            template: '<tr><td>this is a row</td></tr>'
        })

        var vm = new Vue({
            el: '#app',
        })
    </script>
    ```
2. 子组件中定义data，应为一个函数
    ```
    <script>
        Vue.component('rows',{
            data: function(){
                return{
                    content: 'this is a row'
                }
            },
            template: '<tr><td>{{ content }}</td></tr>'
        })

        var vm = new Vue({
            el: '#app',
        })
    </script>
    ```
3. $refs,$emit使用

    标签中使用ref属性，可在js中使用$refs获取dom节点
    组件中使用ref属性，在js中使用$refs获取当前组件，从而可拿到组件的data值
    
    $emit用于子组件向父组件传值，触发父组件的自定义事件