
# :: cmd :: instruction can be override 


# :: entrypoint :: instruction can not be override 



### ENTRY POINT


#### CMD INSTRUCTION
```
52.3.246.41 | 172.31.62.57 | t2.micro | https://github.com/Chowdary-Hari/learn-docker.git
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
```
[ ec2-user@ip-172-31-62-57 ~/learn-docker/ENTRYPOINT ]$ docker run entrypoint:1.0 ping -c4
