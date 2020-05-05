# SRv6 uSID Linux implementation Home Page

The SRv6 "micro segment" (uSID for short) solution is an extension to the SRv6 Network
Programming model ([see below](#reference-ietf-documents)). It allows expressing SRv6 segments with a very compact and 
efficient representation, for example using two bytes for uSID instead of using 
a normal IPv6 address (16 bytes) for a regular SRv6 segment.

In the context of the [ROSE](https://netgroup.github.io/rose/) project, [we](#srv6-usid-linux-implementation-team) have 
implemented the SRv6 uSID solution in Linux..

The processing of micro segments is performed by the Linux kernel, extending the current SRv6 implementation.
The iproute2 userspace tool has been modified to support the configuration of the SRv6 uSIDs. The usage of
the new iproute2 CLI commands is explained [here](iproute2-uSID-README.md).


### SRv6 uSID Linux implementation source code

- kernel: [https://github.com/netgroup/srv6-usid-linux-kernel](https://github.com/netgroup/srv6-usid-linux-kernel)
- iproute2: [https://github.com/netgroup/srv6-usid-linux-iproute2](https://github.com/netgroup/srv6-usid-linux-iproute2)

### Reference IETF documents

"Network Programming extension: SRv6 uSID instruction" [Internet Draft](https://tools.ietf.org/html/draft-filsfils-spring-net-pgm-extension-srv6-usid)

"SRv6 Network Programming" [Internet Draft](https://tools.ietf.org/html/draft-ietf-spring-srv6-network-programming) 
              
"IPv6 Segment Routing Header (SRH)" [RFC 8754](https://www.rfc-editor.org/rfc/rfc8754.html)

### SRv6 uSID Linux implementation Team

- Andrea Mayer
- Paolo Lungaroni
- Stefano Salsano
