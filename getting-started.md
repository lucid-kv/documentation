---
description: This is the start guide for a Linux user.
---

# Getting Started

## Download the Archive

Firstly, download and extract the archive from the latest [GitHub release](https://github.com/clintnetwork/lucid/releases/latest).

```bash
$ wget https://github.com/lucid-kv/lucid/releases/latest/download/lucid.zip
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

A Fast, Secure and Distributed KV store with an HTTP API.
Written in Rust, Fork us on GitHub (https://github.com/lucid-kv)

FLAGS:
    -h, --help         Prints help information
        --no-banner    Disable showing the banner on start
    -V, --version      Prints version information

OPTIONS:
    -c, --config <config>    Specify the Lucid configuration file

SUBCOMMANDS:
    help        Prints this message or the help of the given subcommand(s)
    init        Initialize Lucid and generate configuration file
    server      Run a new Lucid server instance
    settings    Manage the Lucid configuration file

```

