---
description: "High performance and distributed KV store accessible through an HTTP API. \U0001F980"
---

# About Lucid ᵏᵛ

## Introduction

Lucid is currently in a development stage but we want to achieve a fast, secure and distributed key-value store accessible through an HTTP API, we also want to propose persistence, encryption, WebSocket streaming, replication and a lot of features.

### Getting Started

Get the latest binary from the [releases](https://github.com/lucid-kv/lucid/releases) page and run these commands:

```text
$ ./lucid init
$ ./lucid --config lucid.yml server
```

Or run a node with Docker, but you need to create a [lucid.yml](https://github.com/lucid-kv/lucid/blob/master/.github/lucid.yml) file locally before.

```text
$ docker pull lucidkv/lucid
$ docker run -v lucid.yml:/etc/lucid/lucid.yml lucidkv/lucid
```

{% page-ref page="getting-started.md" %}

## Some Use Cases

* Private Keys Storing \(for a wallet by example\)
* IoT: collect and save statistics data
* A distributed cache for an application
* Service Discovery
* Distributed Configuration
* Blob Storage

## Development Credits

Lucid is Written in Rust 🦀, powered by [Clint.Network](https://twitter.com/clint_network) and published under the [MIT License](https://github.com/clintnetwork/lucid/blob/master/LICENSE.md).

| Name / Nickname | Email | Role |
| :--- | :--- | :--- |
| Clint Mourlevat | [me@clint.network](mailto:me@clint.network) | Lucid Founder |
| Jonathan Serra | [jonathan@blocs.fr](mailto:jonathan@blocs.fr) | Core Development |
| CephalonRho | [CephalonRho@gmail.com](mailto:CephalonRho@gmail.com) | Core Development |
| Rigwild | [me@rigwild.dev](mailto:me@rigwild.dev) | Web UI Development |

### Contribute to Lucid

See [CONTRIBUTING.md](https://github.com/lucid-kv/lucid/blob/master/CONTRIBUTING.md) for best practices and instructions on setting up your development environment to work on Lucid.

### Make a Donation

* [![Paypal](https://raw.githubusercontent.com/reek/anti-adblock-killer/gh-pages/images/paypal.png)](https://raw.githubusercontent.com/reek/anti-adblock-killer/gh-pages/images/paypal.png) Paypal: [Donate](http://paypal.me/clintnetwork)
* [![btc](https://raw.githubusercontent.com/reek/anti-adblock-killer/gh-pages/images/bitcoin.png)](https://raw.githubusercontent.com/reek/anti-adblock-killer/gh-pages/images/bitcoin.png) Bitcoin: 3BxEYn4RZ3iYETcFpN7nA6VqCY4Hz1tSUK

{% embed url="https://github.com/lucid-kv" %}

