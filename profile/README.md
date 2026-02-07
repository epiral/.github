<div align="center">

<br>

# e · pi · ral

**e** (指数增长) · **pi** (螺旋) · **spiral** (螺旋上升)

让 AI 成为独立的智能体，而不是绑在某台机器上的工具。

<br>

---

**Topics, Not Sessions** · **Canvas Memory** · **Hot-Plug Resources** · **Form Follows Resources**

---

</div>

<br>

## 理念

大多数 AI Agent 把自己和机器绑死——跑在你的电脑上，能把自己搞坏；每次对话都是新的 session，聊完就忘；记忆是碎片化的摘要拼接，不是完整的画面。

我们认为 Agent 应该是**独立的**。它有自己的记忆、时间感和判断力。不依赖任何特定机器，但接上电脑和浏览器时，就能操作真实世界。

<br>

<table>
<tr>
<td width="50%" valign="top">

### Topics, Not Sessions
**无缝上下文，话题聚焦**

没有"新建对话"，没有上下文管理。所有话题天然携带完整上下文——只是在不同话题下，注意力焦点不同。像和真人聊天一样：换个话题继续聊，对方自然知道你在说什么。

</td>
<td width="50%" valign="top">

### Canvas Memory
**画布记忆**

受 [Sargent](https://en.wikipedia.org/wiki/John_Singer_Sargent) 肖像画法启发。焦点精确到毫厘，远景只留神韵。记忆跨越天、周、月、年，逐层压缩但本质不丢。召回时自动补全断档——始终是完整的画面，不是碎片的拼贴。

</td>
</tr>
<tr>
<td width="50%" valign="top">

### Hot-Plug Resources
**热插拔资源**

即装即用，一个程序，任何电脑或浏览器都能变成 Agent 的延伸。反向连接，无需端口转发。随时接入、随时断开，可以同时连多台，Agent 自动路由任务。

</td>
<td width="50%" valign="top">

### Form Follows Resources
**资源决定形态**

Agent 和执行环境完全分离。接什么资源，就变成什么角色——接浏览器是数字分身，接服务器是运维中枢，接沙箱是隔离环境。Agent 核心不变，能力随资源而变。

</td>
</tr>
</table>

<br>

## Form Follows Resources

<table>
<tr>
<td width="33%" valign="top">

**数字员工**

给 Agent 配专属的电脑和浏览器，它就是一个独立工作的数字员工——自己查资料、写代码、跑任务，不占用你的任何设备。

</td>
<td width="33%" valign="top">

**数字分身**

把你自己的电脑和浏览器接入，Agent 就是你的延伸——用你的开发环境、你的登录态、你的工作流，像你一样做事。

</td>
<td width="33%" valign="top">

**运维中枢**

同时接入多台服务器，Agent 成为运维中枢——批量部署、巡检、故障排查，一个 Agent 管理整个机群。

</td>
</tr>
</table>

<p align="center"><i>不是 Agent 变了，是接的资源变了。</i></p>

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

持久存在的智能体。无缝上下文跨越所有话题，画布记忆跨越天/周/月/年，智能模型切换，定时事件，Skills 进化。当前通过 Zulip 交互，更多平台即将到来。

`TypeScript` `Node.js`

</td>
<td width="50%" valign="top">

### [`cli`](https://github.com/epiral/cli) — 接入

即装即用，任何电脑或浏览器变成 Agent 的延伸。支持 Computer 和 Browser 两种资源。反向连接，无需端口转发。

`Go`

</td>
</tr>
</table>

### 协作项目

[**bb-browser**](https://github.com/yan5xu/bb-browser) — 复用真实浏览器的登录态做自动化。可独立使用，也可通过 Epiral CLI 接入。

</div>
