# actions-proto-go

The wire protocol for **Hanzo Git Actions** — the protobuf /
[connect](https://connectrpc.com) contract spoken between the Hanzo Git runner
(`git-runner`) and the Hanzo Git server at `git.hanzo.ai`.

Two services:

- `runner.v1.RunnerService` — runner registration, task fetch, task/log updates.
- `ping.v1.PingService` — health / liveness ping.

## Use

```go
import (
	runnerv1 "git.hanzo.ai/hanzoai/actions-proto-go/runner/v1"
	"git.hanzo.ai/hanzoai/actions-proto-go/runner/v1/runnerv1connect"
)
```

## Provenance

Fork of `gitea.dev/actions-proto-go` (MIT, © The Gitea Authors). Only the Go
import path is rebranded to `git.hanzo.ai/hanzoai/actions-proto-go`; the
on-the-wire protobuf identities (`runner.v1.*`, `ping.v1.*`) are unchanged, so
it stays protocol-compatible with the server. See `LICENSE` and `NOTICE`.
