本节代码对应课程4.4 （给组件绑定原生事件） 

```
<item @click.native="handleClick"></item>
```
item为自定义组件，绑定点击事件有两种方法：
1. 先给子组件item绑定点击事件，使用$emit触发自定义事件，然后在父组件引用的item组件中绑定自定义事件即可。
2. 直接在父组件引用的item组件中绑定，使用@click.native