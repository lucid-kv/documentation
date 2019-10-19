---
description: This is how to deploy a lucid node on a production server.
---

# Production Deployment

## Download and Install

You need to download, and copy the `lucid` binary into the `/usr/bin/` folder.

```bash
$ wget https://xxxx/lucid.tar.gz
$ tar -xvf lucid.tar.gz
$ mv lucid /usr/bin/
$ rm -rf lucid.tar.gz
```

## Create a Systemd Service

To create a systemd service you need to create a new file like this:

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

