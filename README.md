# RabbitMQ-Management-API-Client

**Security research claim — defensive namespace hold. This repository is intentionally benign.**

## Why this repository exists

The Packagist package [`vidaxl/rabbitmq-management-client`](https://packagist.org/packages/vidaxl/rabbitmq-management-client) (~6,700 downloads at time of writing) lists

```
https://github.com/revinbian/RabbitMQ-Management-API-Client.git
```

as its source URL for **every released version**. The original account was renamed (to `zhi35`), which released the `revinbian` username for re-registration — the precondition for a repo-jacking attempt against this package.

## What the exposure actually is

Stable releases pin fixed commit SHAs and resolve distribution archives by repository ID, so a recreated repository **fails closed** for stable installs of the published versions. Pinning to those releases does not pull content from a re-registered namespace.

The real exposure is two **conditional** future channels:

1. **Mutable dev-ref metadata** — development branches such as `dev-revinbian-patch-1` and `dev-Async` could have their metadata rewritten on a future Packagist crawl.
2. **New-tag ingestion** — a malicious new tag (for example `0.2.3`, satisfying existing `^0.2` constraints) could be picked up through Packagist auto-update.

Both channels additionally depend on Packagist rebinding to the recreated repository identity, which is **publicly undemonstrated**.

## Why we hold the namespace anyway

1. **Document the exposure precisely** — the precondition (an unclaimed source namespace) was real and verifiable.
2. **Close the window defensively** — while this namespace is held by a researcher, a malicious party cannot claim it.

## What this repository contains

Nothing that runs. No executable code, no install hooks, no callbacks, no beacons. Only this README and the inert marker file `SECURITY-RESEARCH-MARKER.txt`.

## If you are vidaXL

Update the package's source URL on Packagist (or abandon/replace the package), and review any environment that installs it, especially against dev refs or open version constraints. This namespace can be transferred to you on verified request.

## If you are the original `revinbian` (now `zhi35`)

Get in touch to reclaim this namespace.

Contact: gaijindev@mail.instinct.com
