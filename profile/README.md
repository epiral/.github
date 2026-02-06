<div align="center">

<br>

# e · pi · ral

**e** (指数增长) · **pi** (螺旋) · **spiral** (螺旋上升)

让 AI 成为独立的智能体，而不是绑在某台机器上的工具。

<br>

---

**精简内核** · **资源可插拔** · **控制面与执行面分离**

---

</div>

<br>

## 理念

大多数 AI Agent 把自己和机器绑死——LLM 包一层 tool calling，跑在你的电脑上，能把自己搞坏。

我们认为 Agent 应该是**独立的**。它有自己的记忆、时间感和判断力。不依赖任何特定机器，但接上电脑和浏览器时，就能操作真实世界。

<br>

<table>
<tr>
<td width="33%" valign="top">

### 精简内核

LLM + 消息平台就能工作。记忆、定时任务、模型管理是内建能力。记忆受 [Sargent](https://en.wikipedia.org/wiki/John_Singer_Sargent) 肖像画法启发——焦点精确到毫厘，远景只留神韵。

</td>
<td width="33%" valign="top">

### 资源可插拔

电脑和浏览器是外部资源，随时接入、随时断开。可以同时连多台电脑和多个浏览器，Agent 自动路由任务。

</td>
<td width="33%" valign="top">

### 控制面分离

Agent 和执行环境完全分离。危险操作丢给沙箱，日常任务走工作站，GPU 任务走云服务器。Agent 永远安全。

</td>
</tr>
</table>

<br>

## 架构

```
                         Epiral Agent
                    ┌─────────────────────┐
                    │                     │
                    │  记忆 · 事件 · 模型  │
                    │  Skills · 感知 · 执行│
                    │                     │
                    └──┬──────┬───────┬───┘
                       │      │       │
              ┌────────┘      │       └────────┐
              │               │                │
       ┌──────┴──────┐ ┌─────┴──────┐  ┌──────┴──────┐
       │  工作站      │ │  VPS       │  │  沙箱       │
       │  + 浏览器    │ │            │  │  (Docker)   │
       │  Epiral CLI  │ │ Epiral CLI │  │ Epiral CLI  │
       └─────────────┘ └────────────┘  └─────────────┘
```

## 项目

<table>
<tr>
<td width="50%" valign="top">

### [`agent`](https://github.com/epiral/agent) — 大脑

持久存在的智能体。无缝记忆跨越天/周/月/年，智能模型切换，定时事件，Skills 进化。当前通过 Zulip 交互，更多平台即将到来。

`TypeScript` `Node.js`

</td>
<td width="50%" valign="top">

### [`cli`](https://github.com/epiral/cli) — 接入

一个二进制，几个参数，任何机器变成 Agent 的延伸。支持 Computer 和 Browser 两种资源。反向连接，无需端口转发。

`Go`

</td>
</tr>
</table>

### 协作项目

[**bb-browser**](https://github.com/yan5xu/bb-browser) — 复用真实浏览器的登录态做自动化。可独立使用，也可通过 Epiral CLI 接入。

</div>
