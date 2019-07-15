本节代码对应课程5.5 （过渡与动画） 

```
//多元素与多组件之间的过渡
//多元素之间过渡，需要使用不同的key防止dom复用，mode定义元素显示和隐藏的先后顺序
<transition name="fade" mode="out-in">
    <div v-if="show" key="hello">Hello World</div>
    <div v-else>Bye World</div>
</transition>


//多组件之间过渡，不需要key和mode
<transition name="fade">
    <component :is="type"></component>
</transition>
```




