# actions-proto-go

[![Open in Hanzo](https://hanzo.app/badges/open-in-hanzo.svg)](https://hanzo.app/dev/open?repo=github.com/hanzoai/actions-proto-go&ref=main&action=open) [![Edit with Hanzo](https://hanzo.app/badges/edit-with-hanzo.svg)](https://hanzo.app/dev/open?repo=github.com/hanzoai/actions-proto-go&ref=main&action=edit) [![Deploy with Hanzo](https://hanzo.app/badges/deploy-with-hanzo.svg)](https://hanzo.app/dev/open?repo=github.com/hanzoai/actions-proto-go&ref=main&action=deploy)

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
