一、antd的select下拉框不跟随页面滚动

解决方式：

文章地址：https://antdv.com/docs/vue/faq-cn/。父元素设置position属性，Select上新增getPopupContainer函数，制定展开框挂在到父级节点

```html
<div style={{position: 'relative'}} id='area'>
  <Select defaultValue="lucy"
          getPopupContainer={trigger => trigger.parentNode as HTMLElement}
    >
      <Option value="jack">Jack</Option>
      <Option value="lucy">Lucy</Option>
  </Select>
</div>
```
