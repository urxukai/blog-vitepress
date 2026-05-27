---
title: Eclipse
description: Eclipse 是一个可定制的 rollup 提供程序，与多个第 1 层区块链兼容。 该平台使开发人员能够部署他们自己的由 Solana 操作系统提供支持的 rollup，使用任何链进行安全或数据存储。
---

<PageHeader
  logo="/images/eclipse/logo.svg"
  coverImg="/images/eclipse/cover.jpeg"
  :links="links"
/>

## 跨链

官方跨链桥：https://bridge.eclipse.xyz/

第三方跨链桥：https://www.usenexus.org/

## 养牛点击游戏

https://tap.eclipse.xyz/

#### 脚本

```js
function randomCenterClick() {
  // 获取屏幕尺寸
  const screenWidth = window.innerWidth || document.documentElement.clientWidth
  const screenHeight = window.innerHeight || document.documentElement.clientHeight

  // 计算中心80%区域的边界
  const margin = 0.1 // 10% margin on each side
  const minX = screenWidth * margin
  const maxX = screenWidth * (1 - margin)
  const minY = screenHeight * margin
  const maxY = screenHeight * (1 - margin)

  // 生成随机位置（在中心80%区域内）
  const x = Math.floor(minX + Math.random() * (maxX - minX))
  const y = Math.floor(minY + Math.random() * (maxY - minY))

  // 创建并触发点击事件
  const clickEvent = new MouseEvent('click', {
    view: window,
    bubbles: true,
    cancelable: true,
    clientX: x,
    clientY: y
  })
  document.elementFromPoint(x, y).dispatchEvent(clickEvent)

  // 生成随机延迟（1到5秒之间）
  const delay = 1000 + Math.random() * 4000

  // 在控制台输出点击信息
  console.log(`点击位置: (${x}, ${y}), 下次点击延迟: ${delay.toFixed(2)}ms`)

  // 安排下一次点击
  setTimeout(randomCenterClick, delay)
}

// 开始点击循环
randomCenterClick()
```

<script setup>
const links = [
  { name: 'eclipse.xyz', url: 'https://www.eclipse.xyz/' },
  { name: 'X', url: 'https://x.com/EclipseFND' },
  { name: 'Doc', url: 'https://docs.eclipse.builders/' },
]
</script>

<style module>
</style>
