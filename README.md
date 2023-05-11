# Batch Connect - ParaView

A Batch Connect app designed for Benefit Lab OnDemand that launches ParaView within a
Hayrat shared node through Quick batch.

## Prerequisites

This Batch Connect app requires the following software be installed on the
**compute nodes** that the batch job is intended to run on (**NOT** the
OnDemand node):

- [ParaView] 4.4.0+
- [Xfce Desktop] 4+

For VNC server support:

- [TurboVNC] 2.1+
- [websockify] 0.8.0+

For hardware rendering support:

- [X server]
- [VirtualGL] 2.3+

[Paraview]: https://www.paraview.org/
[Xfce Desktop]: https://xfce.org/
[TurboVNC]: http://www.turbovnc.org/
[websockify]: https://github.com/novnc/websockify
[X server]: https://www.x.org/
[VirtualGL]: http://www.virtualgl.org/
[Lmod]: https://www.tacc.utexas.edu/research-development/tacc-projects/lmod

## Install

```bash
dnf install -y @Xfce
dnf install -y paraview
wget https://turbovnc.org/pmwiki/uploads/Downloads/TurboVNC.repo -O /etc/yum.repos.d/TurboVNC.repo
dnf install -y turbovnc
dnf install -y python3-websockify
dnf install -y @base-x
wget https://virtualgl.org/pmwiki/uploads/Downloads/VirtualGL.repo -O /etc/yum.repos.d/VirtualGL.repo
dnf install -y VirtualGL
```
