本节代码对应课程5.1 （过渡与动画） 

```
//将需要使用动画过渡的标签使用transition包起来，然后在css中写过渡的样式
<transition name="fade"></transition>

<style>
    .fade-enter,
    .fade-leave-to {
        opacity: 0;
    }

    .fade-enter-active,
    .fade-leave-active {
        transition: opacity 1s;
    }
</style>
```

理解文档中过渡动画的class加载机制



