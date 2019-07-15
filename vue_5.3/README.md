本节代码对应课程5.3 （过渡与动画） 

```
//同时使用过渡与动画，在初次渲染时添加动画，设置动画的时间
<transition 
    :duration="{enter: 2000, leave: 2000}"
    appear
    name = "fade" 
    enter-active-class="animated swing fade-enter-active" 
    leave-active-class="animated shake fade-leave-active"
    appear-active-class="animated swing fade-enter-active"
></transition>

```




