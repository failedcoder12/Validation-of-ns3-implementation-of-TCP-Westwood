# Validation of ns3 implementation of TCP-Westwood
<h3>Computer Networks Course Project.</h3>
Brief: TCP Westwood is designed to improve the performance of TCP in wireless networks. It estimates the available bandwidth in the network to adjust its cwnd. In this project, the aim isto validate ns-3 TCP Westwood implementation by comparing the results obtained from it to those obtained by simulating Linux TCP Westwood.
Required experience: C and C++. <br>
Bonus experience: Knowledge of TCP Westwood and TCP implementation in ns-3. <br>
Difficulty: Moderate.<br>
Recommended Reading: <br> ● Direct Code Execution (Link: https://www.nsnam.org/overview/projects/direct-code-execution/) <br>
● Linux kernel code (Link: https://elixir.bootlin.com/linux/v4.4/source/net/ipv4/tcp_westwood.c) <br>
● Tcp Westwood Paper (Link: ​https://dl.acm.org/citation.cfm?id=381704) <br>
● ns-3 code for TCP Westwood (Path: ns-3.xx/src/internet/model/tcp-westwood.{h, cc})
<br>
<br>
<br>
<h3>Team Members</h3>
<a href="https://github.com/failedcoder12/">Divyansh Verma(16CO110)</a><br>

<a href="https://github.com/PawanR730">Pawan Rahangdale(16CO237)</a><br>

<a href="https://github.com/roshanls1997">Roshan lal Sahu(16CO242)</a><br>



# TCP WESTWOOD DCE

Comparison of **ns-3** and **Linux kernel** implemetations of **TCP WESTWOOD** using **Direct Code Execution** (DCE)

# Final Result

- Congestion Window
![](https://user-images.githubusercontent.com/37220320/48315142-858c1380-e5f8-11e8-9594-6381b611f844.png)

- Queue Size
![](https://user-images.githubusercontent.com/37220320/48315158-bf5d1a00-e5f8-11e8-940b-f884af04280a.png)

Check Out our WIKI [here](https://github.com/failedcoder12/Validation-of-ns3-implementation-of-TCP-Westwood/wiki)

## Network Topology
Dumbbell Topology - With 2 Routers and 5 nodes on each side of the router

(5 nodes) -- (1 router) -- (1 router) -- (5 nodes)

With each node having a point to point connection to the router


## Configurations
#### Inside the `main` function
- `stack` - ("linux"/"ns3")
- `transport_prot` - TcpWestwood
- `linux_prot` - westwood
- `queue_disc_type` - FIFO

#### Adjustments made
- PRR is enabled
- ECN is enabled

## Files
- `dce-gfc-dumbbell-new.cc` - Merged code for running tcp westwood implementations of ns-3 and linux kernel
- `plot-scripts/gnuplot_cwnd` - gnuplot commands to plot congestion window data
- `plot-scripts/gnuplot_queue_size` - gnuplot commands to plot queue size data
