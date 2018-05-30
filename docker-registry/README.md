# Overview

This is a Docker registry implementation to use inside kubernetes.

# WIP Status

Missing to be a candidate in a serious persistent environment:
- A persistent volume claim to persist data across pod changes
- An authentication scheme to have something that starts to look like production. 
- A proper set of ssl certificates
- High availability

However, the current state of the project is adequate if you just need something quick to work with in dev in a temporary setup. Do keep in mind that the service is currently exposed via a node port (30500) so it may be accessible externally if you don't have some strict firewall rules (or the cloud equivalent) configured. On the bright side, you only have to specify localhost:30500 for the image registry and it will just work on any work node.