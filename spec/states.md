# States

## Node states

| State | Meaning |
| --- | --- |
| Active | Connected, healthy and eligible to receive work |
| Idle | Connected but not currently assigned, or not meeting an active task requirement |
| Offline | Heartbeat expired or operator disconnected |

## Job states

```
created → policy_checked → routed → reasoning_running → ...
```

Every transition is idempotent, and a retry never charges twice.

## Media job states

Media jobs (image, video) are asynchronous:

```
queued → preparing → generating → encoding → completed
```

The API returns a job identifier and the client polls or subscribes to status updates.
