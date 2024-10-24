---
title: SuiMine
description:
---

<!-- <PageHeader
  logo="/images/hemi/logo.svg"
  coverImg="/images/hemi/cover.jpeg"
  :links="links"
/> -->

## 交互指南

### 一、官网

https://suimine.xyz/#/tokens/fomo

### 二、脚本

```js
// 获取具有指定类名的所有按钮
const buttons = document.querySelectorAll('.items-center.justify-center.bg-green-600.text-xl.font-bold')

// 定义一个函数来模拟点击
function simulateClick(element) {
  // 创建一个新的MouseEvent对象
  const event = new MouseEvent('click', {
    view: window,
    bubbles: true,
    cancelable: true
  })
  // 触发点击事件
  element.dispatchEvent(event)
}

// 设置一个间隔定时器来循环点击
setInterval(() => {
  buttons.forEach(button => {
    simulateClick(button)
  })
}, 5000) // 每1000毫秒（1秒）点击一次

setInterval(console.clear, 5000)
```

<script setup>
const links = [
  { name: 'suimine.xyz', url: 'https://suimine.xyz/#/tokens/fomo' },
]
</script>

<style module>
</style>
