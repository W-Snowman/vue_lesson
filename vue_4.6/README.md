本节代码对应课程4.6 （具名插槽） 

```
<slot name="header"></slot>     //插槽命名为header
父组件中： <template v-slot:header></template>

<slot></slot>     //插槽默认名为default
父组件中： <template v-slot:default></template>
```
