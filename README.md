# UDP-Pinger
Exchange UDP messages between a client and server, and display the Round-Trip Time (RTT).

# Description
The project consists of a sender and a receiver program. The sender sends a ping message via a UDP socket to the receiver. Upon receiving the ping, the receiver replies with a pong message. The sender then calculates and displays the RTT (Round-Trip Time) for the message exchange.

If the sender does not receive a pong message within 2 seconds (the default timeout), it proceeds to send the next ping.


# Usage
Udp_sender: 
<pre>
./udp_sender &lt;hostname> &lt;port> &lt;message_number>
</pre>
e.g. Sending 10 messages to a host name: 
<pre> 
./udp_sender example.com 18300 10 
</pre>
e.g. Sending 5 messages to an ip address: 
<pre> 
./udp_sender 127.0.0.1 18300 5
</pre>
Udp_receiver: 
<pre>
./udp_receiver &lt;port>
</pre>
e.g. Listening on port 18300: 
<pre>
./udp_receiver 18300
</pre>

# Compile the source code
A Makefile is provided for compilation.<br />

# License
UDP-Pinger is released under the MIT License  
http://opensource.org/licenses/MIT
