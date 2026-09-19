# RabbitMQ-Management-API-Client

**Security research claim — defensive namespace hold. This repository is intentionally benign.**

## Why this repository exists

The Packagist package [`vidaxl/rabbitmq-management-client`](https://packagist.org/packages/vidaxl/rabbitmq-management-client) (~6,700 downloads at time of writing) lists

```
https://github.com/revinbian/RabbitMQ-Management-API-Client.git
```

as its source URL for **every released version**. The original account was renamed (to `zhi35`), which released the `revinbian` username. Until this claim, anyone could re-register `revinbian`, recreate this repository name, break GitHub's rename redirect, and serve attacker-controlled code to every fresh `composer install` of the package — a classic repo-jacking / supply-chain exposure.

This repository exists to:

1. **Demonstrate the exposure concretely** — control of the source-of-truth URL is the proof; no execution is needed.
2. **Close the window defensively** — while this namespace is held by a researcher, a malicious party cannot claim it.

## What this repository contains

Nothing that runs. No executable code, no install hooks, no callbacks, no beacons. Only this README and the inert marker file `SECURITY-RESEARCH-MARKER.txt`.

## If you are vidaXL

Update the package's source URL on Packagist (or abandon/replace the package), and review any environment that still installs it. This namespace can be transferred to you on verified request.

## If you are the original `revinbian` (now `zhi35`)

Get in touch to reclaim this namespace.

Contact: gaijindev@mail.instinct.com
