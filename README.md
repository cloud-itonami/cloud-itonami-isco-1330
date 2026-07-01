# cloud-itonami-isco-1330

Open Occupation Blueprint for **ISCO-08 1330**: Information and Communications Technology Services Managers.

This repository designs a forkable OSS business for an independent IT services manager overseeing a small client's infrastructure: a hardware-support robot performs server-room walkthroughs and inventory checks under a governor-gated actor, so the practice keeps its own change and infrastructure records instead of renting a closed MSP-management SaaS.

## Robotics premise

All cloud-itonami verticals are designed on the premise that a **robot performs
the physical domain work**. Here a hardware-support robot performs server-room walkthroughs, cable tracing and equipment inventory checks under an actor that proposes
actions and an independent **IT Services Governor** that gates them. The governor never
dispatches hardware itself; `:high`/`:safety-critical` actions (such as
data-center power-cycling, or client data migrations) require human sign-off.

A live sample of the operator console (robotics safety console, shared template) is rendered in [docs/samples/operator-console.html](docs/samples/operator-console.html) — pure-data HTML output of `kotoba.robotics.ui`.

## Core Contract

```text
service contract + infrastructure plan + change request
        |
        v
IT Services Advisor -> IT Services Governor -> deploy-support/monitor, or human sign-off
        |
        v
robot actions (gated) + operating records + audit ledger
```

No automated advice can dispatch a robot action the governor refuses, suppress
an operating record, or disclose sensitive data without governor approval and
audit evidence.

## Capability layer

Resolves via [`kotoba-lang/occupation`](https://github.com/kotoba-lang/occupation)
(ISCO-08 `1330`). Required capabilities:

- :robotics
- :identity
- :forms
- :dmn
- :bpmn
- :audit-ledger

See [`docs/business-model.md`](docs/business-model.md) and
[`docs/operator-guide.md`](docs/operator-guide.md).

## License

AGPL-3.0-or-later.
