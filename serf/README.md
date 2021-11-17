Serf Container Image
====================

Build a container-image for [Hashicorp Serf](https://www.serf.io/)


## Usage

```
pdman run -it --rm --uts=host --network=host --volume my/conf/file.json:/etc/serf.json ghcr.io/jmanero/serf agent -config-file /etc/serf.json
```

Notes:

* `--network=host` is the simplest way to run the `serf` container. It allows the agent to auto-configure it's perring address to the host's address, and allows you to configure an optional interface binding in the case of multi-homed hosts.
* `--uts=host` passes the host's hostname and domain-name through to the container. This is used by `serf` to automatically set its node-name
