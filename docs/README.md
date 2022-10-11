# SRv6 uSID Linux implementation Home Page

The SRv6 "micro segment" (uSID for short) solution is an extension to the SRv6 Network
Programming model ([see below](#reference-ietf-documents)). It allows expressing SRv6 segments with a very compact and 
efficient representation, for example using two bytes for uSID instead of using 
a normal IPv6 address (16 bytes) for a regular SRv6 segment. Our scientific papers on this topic
are listed [below](#scientific-papers).

In the context of the [ROSE](https://netgroup.github.io/rose/) project, [we](#srv6-usid-linux-implementation-team) have 
implemented the SRv6 uSID solution in Linux.

The processing of micro segments is performed by the Linux kernel, extending the current SRv6 implementation.
The iproute2 userspace tool has been modified to support the configuration of the SRv6 uSIDs. The usage of
the new iproute2 CLI commands is explained [here](iproute2-uSID-README.md).


### SRv6 uSID Linux implementation source  code

- kernel: [https://github.com/netgroup/srv6-usid-linux-kernel](https://github.com/netgroup/srv6-usid-linux-kernel)
- iproute2: [https://github.com/netgroup/srv6-usid-linux-iproute2](https://github.com/netgroup/srv6-usid-linux-iproute2)

### Reference IETF documents

"Network Programming extension: SRv6 uSID instruction" [Internet Draft](https://tools.ietf.org/html/draft-filsfils-spring-net-pgm-extension-srv6-usid)

"SRv6 Network Programming" [Internet Draft](https://tools.ietf.org/html/draft-ietf-spring-srv6-network-programming) 
              
"IPv6 Segment Routing Header (SRH)" [RFC 8754](https://www.rfc-editor.org/rfc/rfc8754.html)

### Scientific papers

- A. Tulumello, A. Mayer, M. Bonola, P. Lungaroni, C. Scarpitta, S. Salsano, A. Abdelsalam, P. Camarillo, D. Dukes, F. Clad, C. Filsfils, <br>
"[Micro SIDs: a solution for Efficient Representation of Segment IDs in SRv6 Networks](https://doi.org/10.1109/TNSM.2022.3205265)", <br>
IEEE Transaction on Network and Service Management, 2022, ([pdf-preprint](http://netgroup.uniroma2.it/Stefano_Salsano/papers/22_tnsm_srv6_micro_sids.pdf))

- A. Tulumello, A. Mayer, M. Bonola, P. Lungaroni, C. Scarpitta, S. Salsano, A. Abdelsalam, P. Camarillo, D. Dukes, F. Clad, C. Filsfils, <br>
"[Micro SIDs: a solution for Efficient Representation of Segment IDs in SRv6 Networks](https://doi.org/10.23919/CNSM50824.2020.9269075)", <br> 
16th International Conference on Network and Service Management, CNSM 2020 (Acceptance ratio ~19%), 2-6 November 2020, Virtual Conference ([pdf](http://dl.ifip.org/db/conf/cnsm/cnsm2020/1570663490.pdf)). 

### SRv6 uSID Linux implementation Team

- Andrea Mayer
- Paolo Lungaroni
- Stefano Salsano
