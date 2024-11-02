
# :: cmd :: instruction can be override 


# :: entrypoint :: instruction can not be override 



### ENTRY POINT


#### CMD INSTRUCTION
```
[ ec2-user@ip-172-31-62-57 ~/learn-docker/ENTRYPOINT ]$ docker run entrypoint:1.0 ping -c4 facebook.com
PING facebook.com (157.240.229.35) 56(84) bytes of data.
64 bytes from edge-star-mini-shv-02-iad3.facebook.com (157.240.229.35): icmp_seq=1 ttl=52 time=1.35 ms
64 bytes from edge-star-mini-shv-02-iad3.facebook.com (157.240.229.35): icmp_seq=2 ttl=52 time=1.37 ms
64 bytes from edge-star-mini-shv-02-iad3.facebook.com (157.240.229.35): icmp_seq=3 ttl=52 time=1.40 ms
64 bytes from edge-star-mini-shv-02-iad3.facebook.com (157.240.229.35): icmp_seq=4 ttl=52 time=1.44 ms

--- facebook.com ping statistics ---
4 packets transmitted, 4 received, 0% packet loss, time 3005ms
rtt min/avg/max/mdev = 1.352/1.392/1.443/0.033 ms
```

#### ENTRY POINT INSTRUCTION
* exit to over ride entry point

```
[ ec2-user@ip-172-31-62-57 ~/learn-docker/ENTRYPOINT ]$ docker run entrypoint:1.0 `ping -c4 facebook.com`
ping: ping: Name or service not known
```

```
[ ec2-user@ip-172-31-62-57 ~/learn-docker/ENTRYPOINT ]$ docker run entrypoint:1.5
PING google.com (172.253.63.101) 56(84) bytes of data.
64 bytes from bi-in-f101.1e100.net (172.253.63.101): icmp_seq=1 ttl=55 time=1.85 ms
64 bytes from bi-in-f101.1e100.net (172.253.63.101): icmp_seq=2 ttl=55 time=1.91 ms
64 bytes from bi-in-f101.1e100.net (172.253.63.101): icmp_seq=3 ttl=55 time=1.88 ms
64 bytes from bi-in-f101.1e100.net (172.253.63.101): icmp_seq=4 ttl=55 time=1.90 ms


--- google.com ping statistics ---
5 packets transmitted, 4 received, 0% packet loss, time 4006ms
rtt min/avg/max/mdev = 1.849/1.889/1.908/0.021 ms
```
