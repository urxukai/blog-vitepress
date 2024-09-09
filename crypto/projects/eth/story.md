---
title: Story Protocol
---

<PageHeader
  logo="/images/story/logo.jpg"
  coverImg="/images/story/cover.jpeg"
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

## 交互指南

### 一·交互准备

1️⃣ 官方水龙头（一个）：https://faucet.story.foundation

2️⃣ STORY 测试网注册 IP https://play.story.foundation/assets/register

3️⃣ STORY 社交任务拿角色 https://bot.story.foundation

### 二·质押 （这个限制有点离谱，至少 1024 个）

传送门：https://staking.story.foundation

### 三·SAWP

@piperxprotocol
是 story 上的 dex
官网：https://app.piperx.xyz Dex 本身其实没啥可说的，就是正常的 swap+lp 的添加。

### 四· Defi

@UnleashProtocol
是 story 上的 defi
官网：https://app.unleashprotocol.xyz
做做质押和借贷就行

### 五·NFT 市场

@color_mp
是测试网上的一个 NFT 市场。
传送门：https://colormp.com/launchpad
交互建议：mint 完 NFT 后，可以在市场进行交易

### 六·生态项目

@TheBlockBookapp
是生态里面的一个比较成熟的创作者平台。
官网：https://blockbook.app
上传内容：可以选择上传视频、图片、音频、文本

<script setup>
const links = [
  { name: 'storyprotocol.xyz', url: 'https://www.storyprotocol.xyz/' },
  { name: 'X', url: 'https://x.com/StoryProtocol' },
]

const activities = [
  {
    timestamp: '2024-08-27',
    content: 'Story Protocol 在测试网上线',
  },
  {
    timestamp: '2024-08-21',
    content: 'Story Protocol 完成 8000 万美元B轮融资',
  },
  {
    timestamp: '2023-09-06',
    content: 'Story Protocol 完成 2500 万美元A轮融资',
  },
  {
    timestamp: '2023-05-17',
    content: 'Story Protocol 完成 2930 万美元融资',
  }
]
</script>
