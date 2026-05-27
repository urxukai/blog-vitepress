<!--
 * @Author: 徐凯 xukai@sinoroad.com
 * @Date: 2025-02-06 13:09:32
 * @Description:
-->
---
title: Sentient
description: Sentient 正在构建由社区贡献的开源 AI 模型，目标是直接与OpenAI竞争。Sentient将为贡献者发起活动，每个活动都有特定的指标，用于根据这些指标评估贡献和奖励。
---

<PageHeader
  logo="/images/sentient/logo.png"
  coverImg="/images/sentient/cover.jpeg"
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

## Mint NFT

https://campaign.sentient.xyz/

教程

https://x.com/ouyoung11/status/1880440986431881238

## Sentient测试网站

dobby-arena.sentient.xyz

🔸输入问题，向Sentient聊天模型提问
🔸Sentient会给出两个回答，每个回答务必投票

<script setup>
const links = [
  { name: 'sentient.foundation', url: 'https://sentient.foundation/' },
  { name: 'X', url: 'https://x.com/SentientAGI' },
]

const activities = [
  {
    timestamp: '2024-07-02',
    content: 'Sentient 完成 8500 万美元种子轮融资',
  },
]
</script>
