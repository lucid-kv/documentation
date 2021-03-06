---
description: Lucid node production deployement guide.
---

# Production Deployment

## Download and Install

You need to download and copy the `lucid` binary to the `/usr/bin/` directory. See [latest Github release](https://github.com/clintnetwork/lucid/releases/latest).

```bash
$ wget https://github.com/lucid-kv/lucid/releases/latest/download/lucid.zip
$ tar -xvf lucid.zip
$ mv lucid /usr/bin/
$ rm -rf lucid.zip
```

## Create a Systemd Service

To create a systemd service you need to create the following file.

```text
$ nano /etc/systemd/system/lucid.service
```

```text
[Unit]
Description=Lucid KV Store

[Service]
ExecStart=/usr/bin/lucid
Restart=always
RestartSec=10
KillSignal=SIGINT
SyslogIdentifier=lucid
User=root

[Install]
WantedBy=multi-user.target
```

### Enable Startup and Run the Service

```text
$ systemctl enable lucid
$ systemctl start lucid
```

