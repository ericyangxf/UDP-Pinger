# UDP-Pinger
Exchanging an UDP message between client and server, and show the Round Trip Time (RTT).

# Description
There are a sender program and a receiver program. The sender program sends a 'ping' message via UDP socket to the receiver. If the receiver gets the 'ping' message, it will return a 'pong' message to the sender. After that, the sender shows the RTT (Round-Trip Time) of this message exchange. The default timeout value is 2 seconds. If the sender does not receive the 'pong' message within 2 seconds, it will send the next message.


# Usage
Udp_sender: 
<pre>
./udp_sender &lt;hostname> &lt;port> &lt;message_number>
</pre>
e.g. Sending 10 messages to host name: 
<pre> 
./udp_sender example.com 18300 10 
</pre>
e.g. Sending 5 messages to ip address: 
<pre> 
./udp_sender 127.0.0.1 18300 5
</pre>
Udp_receiver: 
<pre>
./udp_receiver &lt;port>
</pre>
e.g. Listening port 18300: 
<pre>
./udp_receiver 18300
</pre>

# Compile the source code
A Makefile for compile is provided.<br />

# License
UDP-Pinger is released under the MIT License  
http://opensource.org/licenses/MIT
