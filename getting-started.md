---
description: This is the start guide for a Linux user.
---

# Getting Started

## Download the Archive

Firstly, download and extract the archive from the latest [GitHub release](https://github.com/clintnetwork/lucid/releases/latest).

```bash
$ wget https://github.com/clintnetwork/lucid/releases/latest/download/lucid.zip
$ tar -xvf lucid.zip
```

## First Launch

Once you have downloaded the binary, you can run the help command.

```bash
$ ./lucid help
```

```text
 ██╗    ██╗   ██╗ ██████╗██╗██████╗     ██╗  ██╗██╗   ██╗
 ██║    ██║   ██║██╔════╝██║██╔══██╗    ██║ ██╔╝██║   ██║
 ██║    ██║   ██║██║     ██║██║  ██║    ██╔═██╗ ╚██╗ ██╔╝
 ██████╗╚██████╔╝╚██████╗██║██████╔╝    ██║  ██╗ ╚████╔╝
 ╚═════╝ ╚═════╝  ╚═════╝╚═╝╚═════╝     ╚═╝  ╚═╝  ╚═══╝

A Fast, Secure and Distributed KV store with a HTTP API.
Written in Rust by Clint.Network (twitter.com/clint_network)

USAGE:
    lucid.exe [SUBCOMMAND]

FLAGS:
    -h, --help       Prints help informations
    -v, --version    Print version information

SUBCOMMANDS:
    cli         Spawn to the command line interface
    help        Prints this message or the help of the given subcommand(s)
    init        Initialize the Lucid cluster and generate configuration file
    members     Manage members of the cluster
    server      Run a new Lucid server instance
    settings    Manage Lucid configuration file
    store       Play with the KV store (get/set)
    tokens      Manage JWT Tokens (issue, revoke etc.)
```
