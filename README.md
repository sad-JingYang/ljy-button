### Sad Button 组件

Sad Button 组件是一个灵活的按钮组件，可以根据需求定制按钮的样式、大小和状态。

#### 使用方法

1. **安装**

   Sad Button 组件可以通过 npm 安装：

   ```bash
   npm install sad-button --save
   ```

2. **引入**

   在需要使用的组件中引入 sad Button：

   ```javascript
   import SadButton from 'sad-button';
   ```

3. **基本用法**

   使用 `<sad-button>` 标签来创建按钮，可以通过插入文本或其他元素来定义按钮的内容。

   ```html
   <sad-button>Click me</sad-button>
   ```

4. **属性**

   Sad Button 组件提供了以下属性来定制按钮的样式、大小和状态：

    - `type`: 按钮类型，可选值包括 `default`, `primary`, `success`, `info`, `warning`, `danger`，默认为 `default`;
    - `size`: 按钮大小，可选值包括 `default`, `medium`, `small`, `mini`，默认为 `default`;
    - `disabled`: 是否禁用按钮，值为 `true` 或 `false`，默认为 `false`;
    - `round`: 是否显示圆角按钮，值为 `true` 或 `false`，默认为 `false`;
    - `circle`: 是否显示圆形按钮，值为 `true` 或 `false`，默认为 `false`;

   ```html
   <sad-button type="primary" size="medium" disabled round>Primary Button</sad-button>
   ```

5. **事件**

   Sad Button 组件支持 `click` 事件，可以通过 `@click` 绑定事件处理函数。

   ```html
   <sad-button @click="handleClick">Click me</sad-button>
   ```

#### 示例

```html

<template>
   <div class="first">
      <sad-button>主要按钮</sad-button>
      <sad-button @click="handleClick" type="primary">主要按钮</sad-button>
      <sad-button type="success">成功按钮</sad-button>
      <sad-button type="info">信息按钮</sad-button>
      <sad-button type="warning">警告按钮</sad-button>
      <sad-button type="danger">危险按钮</sad-button>
   </div>
   <div class="second">
      <sad-button round>主要按钮</sad-button>
      <sad-button round type="primary">主要按钮</sad-button>
      <sad-button round type="primary">主要按钮</sad-button>
      <sad-button round type="success">成功按钮</sad-button>
      <sad-button round type="info">信息按钮</sad-button>
      <sad-button round type="warning">警告按钮</sad-button>
      <sad-button round type="danger">危险按钮</sad-button>
   </div>
   <div class="third">
      <sad-button disabled>主要按钮</sad-button>
      <sad-button disabled type="primary">主要按钮</sad-button>
      <sad-button disabled type="primary">主要按钮</sad-button>
      <sad-button disabled type="success">成功按钮</sad-button>
      <sad-button disabled type="info">信息按钮</sad-button>
      <sad-button disabled type="warning">警告按钮</sad-button>
      <sad-button disabled type="danger">危险按钮</sad-button>
   </div>
   <div class="fourth">
      <sad-button>主要按钮</sad-button>
      <sad-button size="medium" type="primary">主要按钮</sad-button>
      <sad-button size="small" type="primary">主要按钮</sad-button>
      <sad-button size="mini" type="success">成功按钮</sad-button>
      <sad-button size="mini" type="info">信息按钮</sad-button>
      <sad-button size="small" type="warning">警告按钮</sad-button>
      <sad-button size="medium" type="danger">危险按钮</sad-button>
   </div>
</template>

<script lang="ts" setup>
   import sadButton from 'sad-button';

   function handleClick() {
      console.log('Button clicked!');
   }
</script>
```

#### 注意事项

- 当需要自定义按钮样式时，可以通过在 `<sad-button>` 标签中添加类名来实现。

#### 更新日志

- v1.0.0 (2024-04-19): 初始版本发布。
