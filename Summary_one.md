# Brief Summary of <a href="https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=965869"> TCP Westwood: Congestion Window Control Using Bandwidth Estimation </a>
 ● TCP westwood is the sender side only modification of TCP Reno that intended to better handle large bandwidth delay product path, with potential packet loss due to transmission or other errors.<br>
 ● It relies on mining ACK stream for information to help it better set the congestion control paramenter. (Slow start threshold [ssthres], congestion window [cwin] ) <br>
 ● It continuosly estimates, at the TCP sender , the packet rate of the connection by monitoring ACK reception rate. Then estimated connection rate is used to compute congestion window and slow start threshold setting after the a congestion episode.<br>
 ● TCPW has a simple modification of TCP source period stack which allows source to estimate available bandwidth and use this bandwidth to recover faster, thus achieving higher throughput.<br>
 ● 2 basics concepts - 1) end to end estimation of available bandwidth. 2) Estimates to set the slow start threshold and congestion window.<br>
 ● It continously estimates packet rate of connection by properly overaging the rate of returning action<br>
 ● It uses the bandwidthestimate directly to derive window instead using it to compute the backlog<br>
 ● TCPW can't distinguish between buffer overflow loss and random loss</h3><br>
 ● Some TCP uses snoop protocol thus help from intermediate routers for estimation but TCPW doesn't require any such thing thus preserving end to end estimation principle<br>
