# Readme for iproute2 uSID related commands.

iproute2 is extended to support the SRv6 uN behavior defined in [1].

An example iproute2 command is as follows:

```text
 # ip -6 route add bbbb:bbbb:0400::/48 encap seg6local action uN dev eth0
```

The SRv6 uN behavior depends on the IPv6 prefix used to allocate the SRv6 SIDs
(known as uSID Block) as well the length of the uSID itself.

By default uSID Block length is 32 bits and the uSID length is 16 bits.

They can also be configured using SRv6 SIDs optional parameters as follows:

```text
 # ip -6 route add bbbb:bbbb:0400::/32 encap seg6local action uN ubl 16 ul 16 dev eth0
```

In this example the uSID Block length (represented by ubl) is 16 bits and the
uSID length (represented by ul) is also 16 bits.
Both "ubl" and "ul" length values must be multiples of 8.

The default values for both uSID Block and uSID lengths are configurable using a
newly defined sysctl:

```text
 # sysctl -w net.ipv6.seg6_local.usid_block_len=16
 # sysctl -w net.ipv6.seg6_local.usid_len=16
```

or accessing directly through the procfs:

```text
 # echo 16 > /proc/sys/net/ipv6/seg6_local/usid_block_len
 # echo 16 > /proc/sys/net/ipv6/seg6_local/usid_len
```

The "ip route show" command displays the route information as follows:

```text
 # ip -6 route show bbbb:bbbb:0400::/48
 bbbb:bbbb:0400::/48 encap seg6local action uN ubl 32 ul 16 dev eth0 metric 1024 pref medium
```

The JSON output:

```text
 # ip -6 -j -p route show bbbb:bbbb:0400::/48
 [ {
	"dst": " bbbb:bbbb:0400::/48",
	"encap": "seg6local",
	"action": "uN",
	"ubl": 32,
	"ul": 16,
	"dev": "eth0",
	"metric": 1024,
	"flags": [ ],
	"pref": "medium"
 } ]
```

[1] https://tools.ietf.org/html/draft-filsfils-spring-net-pgm-extension-srv6-usid-04
