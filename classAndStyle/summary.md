### bind-class

有两种形式:

1. 使用类，属性名为类名，属性值是bool类型,当值为true会对绑定节点添加这个类
2. 使用数组,可以使用条件表达式来动态添加类,或者使用对象数组。

注意点:

1. 绑定时可以在标签中写表达式,也可以直接绑定一个classObject，结合computed属性,在computed中返回classObj
2. 直接使用class属性不会覆盖:class,
3. 对组件使用:class,会把类绑定到组件的根元素上



### bind-style

也有俩种形式:

1. 使用对象进行绑定,同样可以使用字面值对象或用对象变量,结合computed property
2. 数组形式,数组形式会将多个style对象进行合并

### [自动添加前缀](https://cn.vuejs.org/v2/guide/class-and-style.html#%E8%87%AA%E5%8A%A8%E6%B7%BB%E5%8A%A0%E5%89%8D%E7%BC%80)

当 `v-bind:style` 使用需要添加[浏览器引擎前缀](https://developer.mozilla.org/zh-CN/docs/Glossary/Vendor_Prefix)的 CSS 属性时，如 `transform`，Vue.js 会自动侦测并添加相应的前缀。

### [多重值](https://cn.vuejs.org/v2/guide/class-and-style.html#%E5%A4%9A%E9%87%8D%E5%80%BC)

> 2.3.0+

从 2.3.0 起你可以为 `style` 绑定中的属性提供一个包含多个值的数组，常用于提供多个带前缀的值，例如：

```
<div :style="{ display: ['-webkit-box', '-ms-flexbox', 'flex'] }"></div>
```

这样写只会渲染数组中最后一个被浏览器支持的值。在本例中，如果浏览器支持不带浏览器前缀的 flexbox，那么就只会渲染 `display: flex`。

 