 <h1>Analyzing Packets With Wireshark</h1>

<h2>Description</h2>

This Project consists of steps on how to Use Wireshark filters to:
 <ol type = "1">
  
<li>Inspect a specific IP addresses traffic</li>
<li>Explore DNS packets to examine protocol data</li>
<li>Search TCP packets for various payload text data</li>
</ol>

<h2>Languages and Utilities Used</h2>

- <b><a href="https://www.wireshark.org/">Wireshark</a></b>

<h2>Environments Used </h2>

- <b>Windows 10</b>

<h2>Program walk-through:</h2>


<h3>Part 1: Inspecting traffic from a user </h3>

<p align="center">
 To start I opened a sample .pcap file provided by <a href="https://go.qwiklabs.com/">QikiLabs</a> to start experimenting with. By inserting <code>ip.addr == 142.250.1.139</code> In the filter box, only packets with the source or the destination IP address will appear.
 
<img src="https://imgur.com/za6Ng5n.png" />
</br>
<p align="center">
By opening the packet details pane window I can see that this packet's destination is port 80 (HTTP) and is a SYN packet meaning this is the start of a new TCP 3-Way Handshake.
 
<img src="https://imgur.com/aIQwZ2g.png"/>
<p align="center">
 
Other possible filters to analyze specific network packets: 
 <li>Where the packets came from <code>ip.src == 142.250.1.139</code> </li>
 <li>Where the packets were sent to <code>ip.dst == 142.250.1.139</code></li>
 <li>Even by physical Ethernet Media Access Control (MAC) address using <code>eth.addr == 42:01:ac:15:e0:02</code></li>
</br>
<p align="center">
 Back in the same packet detail window in the Ethernet II subtree, the MAC address is displayed in clear text.
 
<img src="https://imgur.com/1nlqD4g.png"/>


<h3>Part 2: Analyzing DNS packets </h3>
<img src="https://imgur.com/xQ485Wm.png"/>


<h3>Part 3: Analyzing TCP packets</h3>
<img src="https://imgur.com/BnOtmwq.png"/>
