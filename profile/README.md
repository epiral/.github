<div align="center">

<br>

# e · pi · ral

**e** (指数增长) · **pi** (螺旋) · **spiral** (螺旋上升)

构建有真正自主性的 AI 智能体

<br>

---

**Agent 的核心是精简的** · **资源可插拔** · **控制面与执行面分离**

---

</div>

<br>

## 理念

大多数 AI Agent 是这样的：一个 LLM 包上一层 tool calling，跑在你的机器上，和机器绑死。

我们认为这是错的。

**Agent 应该是一个独立的、持久存在的智能体。** 它有自己的记忆、自己的时间感、自己的判断力。它不需要依赖任何特定的机器或设备——但当你给它接上电脑和浏览器时，它就能操作真实世界。

<br>

<table>
<tr>
<td width="33%" valign="top">

### 精简核心

Agent 只需要 LLM + 消息平台就能工作。记忆、定时任务、模型管理是内建能力。记忆系统受 Sargent 油画启发——焦点精确，远景写意，本质不丢。

</td>
<td width="33%" valign="top">

### 资源可插拔

电脑和浏览器是可插拔的外部资源。随时接入、随时断开，可以同时连接多台电脑和多个浏览器——Agent 自动路由，任务分发到对的地方。

</td>
<td width="33%" valign="top">

### 控制面分离

Agent 和它操控的资源完全分离。你可以把危险操作路由到沙箱、日常任务路由到工作站、GPU 任务路由到云服务器。Agent 永远安全，不可能把自己搞坏。

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

持久存在的 AI 智能体。有跨天/周/月/年的无缝记忆、智能模型切换、定时事件、Skills 系统。当前通过 Zulip 交互，未来将支持更多消息平台。

`TypeScript` `Node.js`

</td>
<td width="50%" valign="top">

### [`cli`](https://github.com/epiral/cli) — 接入

一个二进制文件，几个参数，把任何机器变成 Agent 的资源。同时支持 Computer（shell + 文件）和 Browser（网页自动化）两种资源类型。反向连接，无需端口转发。

`Go`

</td>
</tr>
</table>

### 协作项目

[**bb-browser**](https://github.com/yan5xu/bb-browser) — 面向 AI Agent 的浏览器自动化。复用用户真实浏览器的登录态，可独立使用，也可通过 Epiral CLI 接入 Agent。

</div>
