本节代码对应课程5.6 （过渡与动画） 

```
//列表的过渡
<transition-group name="fade">
    <div v-for="(item,index) of list" :key="item.id">{{item.title}}</div>
</transition-group>
```




