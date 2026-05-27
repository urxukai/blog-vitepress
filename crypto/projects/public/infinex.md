---
title: Infinex
description:
---

<PageHeader
  logo="/images/infinex/logo.svg"
  coverImg="/images/infinex/cover.jpeg"
  :links="links"
/>

## 相关事件

<el-timeline style="max-width: 600px">
  <el-timeline-item
    v-for="(activity, index) in activities"
    :key="index"
    :timestamp="activity.timestamp"
  >
    {{ activity.content }}
  </el-timeline-item>
</el-timeline>

```js
function changeTitle() {
  const dom = document.querySelector('.font-number')
  document.title = dom.innerText
}

setInterval(changeTitle, 5000)
```

<script setup>
const links = [
  { name: 'infinex.xyz', url: 'https://infinex.xyz/' },
  { name: 'X', url: 'https://x.com/infinex_app' },
  { name: 'TVL', url: 'https://infinex.xyz/tvl' },
]

const activities = [
  {
    timestamp: '2024-09-25',
    content: 'Infinex 完成 6530 万美元融资',
  },
  {
    timestamp: '2023-12-23',
    content: 'Infinex 在主网上线',
  },
]
</script>
