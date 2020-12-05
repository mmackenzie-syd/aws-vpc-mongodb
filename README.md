# aws-vpc-mongodb

####
https://www.youtube.com/watch?v=kWhIwlNkZm4

https://www.patreon.com/cloudtutorials

https://stackoverflow.com/questions/51734945/cidr-address-is-not-within-cidr-address-from-vpc

An IPv4 address consists of 32 bits.

1) /32 in CIDR x.x.x.x/32 means use all 32 bits to form a range of addresses. In this case just one IP address is possible.

2) /24 in CIDR x.x.x.0/24 means fix the first 24 bits and use last 8 bits to form a range of addresses. In this case, there can be 2^8 IP addresses i.e. from x.x.x.0 to x.x.x.255.

3) /16 in CIDR x.x.0.0/16 means fix the first 16 bits and use the last 16 bits to form a range of addresses. In this case, there can be 2^16 IP addresses i.e. from x.x.0.0 to x.x.255.255.

4) /8 in CIDR x.0.0.0/8 means fix the first 8 bits and use the last 24 bits to form a range of addresses. In this case, there can be 2^24 IP addresses i.e. from x.0.0.0 to x.255.255.255.

5) /0 in CIDR 0.0.0.0/0 means fix the first 0 bits and use the last 32 bits to form a range of addresses. In this case, all the possible IP addresses are included in the range.

Hope it helps you in understanding your problem that first 16 bits needs to be fixed in x.x.0.0/16 CIDR.

