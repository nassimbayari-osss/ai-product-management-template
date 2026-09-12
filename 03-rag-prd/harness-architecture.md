## Harness architecture (Juno PM)

**Archetype: Supervised agent**

The task repeats at volume and success is machine-checkable, which is the only combination that justifies the engineering. It is unshippable until the Module 6 evals exist.

| Surface | Setting |
|---|---|
| 01 Context | Let the model fetch on demand through a read tool, with a per-turn assembly cap so the window does not flood. |
| 02 Tools | Only the verbs this task needs. Omissions documented. |
| 03 Loop | Ceiling of 3 to 5 turns. Escalate after 2 consecutive failed tool calls. Target p95 under 8 seconds. |
| 04 Memory | Durable, with a TTL per fact. Human corrections outrank stored model output and never expire silently. |
| 05 Permissions | read auto, draft auto, write confirm, send blocked in V1 |
| 06 Verification | Automated check runs before the output reaches a human. Define the pass bar in Module 6. On failure: Block the output and retry once, then escalate. |

### Drivers

- **Blast radius**: The whole company
- **Recoverability**: Yes, with effort
- **Verifiability**: A machine can check it
- **Repetition**: Many times a day
- **Latency budget**: 2 to 8s
