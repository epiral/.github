<div align="center">

# Epiral

**Autonomous agents that operate real computers.**

</div>

---

We're building the infrastructure for AI agents that go beyond chat — agents that control real machines, browse the web, maintain long-term memory, and act autonomously.

### Repos

| Repo | Description | Language |
|------|-------------|----------|
| [**agent**](https://github.com/epiral/agent) | The brain — a persistent AI agent with multi-layer memory, browser automation, scheduled tasks, and multi-machine orchestration | TypeScript |
| [**cli**](https://github.com/epiral/cli) | The hands — install on any machine to make it a remotely controllable compute node | Go |

### How it works

```
                    ┌────────────────────────┐
                    │     Epiral Agent        │
                    │                        │
                    │  Memory · Browser      │
                    │  Events · Skills       │
                    │  AutoScale · LLM       │
                    └───────────┬────────────┘
                                │
                    ComputerHub (Connect RPC)
                       ┌────────┴────────┐
                       │                 │
                ┌──────┴──────┐   ┌──────┴──────┐
                │  Machine A  │   │  Machine B  │
                │  CLI daemon │   │  CLI daemon │
                └─────────────┘   └─────────────┘
```

The **Agent** lives on a server, connected to a chat platform (Zulip). It thinks, plans, and delegates.

The **CLI** daemons live on real computers. They connect back to the Agent, report their capabilities, and execute whatever the Agent asks — shell commands, file operations, anything.

Between them: a single persistent bidirectional stream. No SSH. No port forwarding. Just a Go binary and a URL.
