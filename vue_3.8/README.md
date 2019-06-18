本节代码对应课程3.6 （列表渲染）  总结如下：

1. 列表渲染
    1. 数组
    ```
    <div v-for='(item, index) of list' :key='item.id'>{{ item.text }}</div>
    ```
    2. 对象
    ```
    <div v-for='(value, name, index) of obj' :key='item.id'>{{ name }} : {{ value }}</div>
    ```
2. 对于数组的列表渲染，要改变数组并显示到页面，可以使用数组的变异方法：
    ```
    push()      //向数组最后添加一个或多个元素，并返回新的长度
    pop()       //删除并返回数组的最后一个元素
    shift()     //删除并返回数组第一个元素
    unshift()   //向数组开头添加一个或多个元素，并返回新的长度
    splice(index,howmany,item1,.....,itemX)    //向/从数组中添加/删除项目，然后返回被删除的项目。howmany为0时表示不删除
    sort()      //排序   无参数时，数组内元素为字符串，按照字母顺序排序
    reverse()   //颠倒数组中元素的顺序
    ```
    非变异方法：(不改变原始数组，返回新数组)

    ```
    filter()    //传参为一个方法，返回新数组，数组中包含符合方法的所有元素
    concat()    //连接多个数组并返回
    slice(start,end)     //从已有的数组中返回选定的元素
    ```
3. Vue.set或vm.$set的使用
    ```
    Vue.set(vm.list,'name','aaa');  //对象
    vm.$set(vm.list, 0, 'bbbb');    //数组
    ```

