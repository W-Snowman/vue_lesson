本节代码对应课程3.5 （计算属性的getter和setter）  总结如下：

- 计算属性默认有getter和setter的方法
```
computed: {
    fullName: {
        get: function() {
            return this.firstName + ' ' + this.lastName;
        },
        set: function(value) {
            var arr = value.split(" ");
            this.firstName = arr[0];
            this.lastName = arr[1];
        }
    }
}
```
1. get方法在所用变量（firstName 和 lastName）发生变化时调用
2. set方法在被计算的变量（fullName）发生变化时调用


