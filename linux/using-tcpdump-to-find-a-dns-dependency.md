# Using tcpdump to find DNS dependency

I was searching for a DNS dependency on a cms server whereby page loads would take an interminable amount of time to return when primary DNS resolution would fail.

I used `tcpdump` to discover what DNS requests were being made in an attempt to
isolate what part of the system was reaching out.

I used:

```bash
tcpdump -i eth0 udp port 53
```

and

```
tcpdump -nt -i eth0 udp port 53
```

to find the culprit, which was each machine in the partner pair reaching out
to the other for memcached or varnish purposes.
