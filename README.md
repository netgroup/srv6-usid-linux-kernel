## Linux kernel 5.6 with SRv6 uSID implementation

### The kernel source code is available in the **srv6-usid-public** branch. 

The patch to iproute2 tool is available at https://github.com/netgroup/srv6-usid-linux-iproute2/.

[Project web page](https://netgroup.github.io/srv6-usid-linux-kernel/), part of the [ROSE](https://netgroup.github.io/rose/) project.

The Linux kernel implementation of SRv6 uSID consists in 4 patches applied to the Linux kernel version 5.6:
 
- add support for optional attributes during behavior construction
- add callbacks for customizing the creation and destruction of a behavior
- add support for SRv6 uN behavior
- add sysctl support for SRv6 micro segment behaviors

See details in the commit messages **of the srv6-usid-public branch**.
