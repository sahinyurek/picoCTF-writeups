<img width="607" alt="Packets_Primer_Description" src="https://github.com/sahinyurek/picoCTF-writeups/assets/62119201/d0c1193e-4218-4b6b-a05b-534b0d689e38">

Use wireshark to analyse packets.
Flag is probably not in ARP messages because it is for associating IP and MAC address.

<img width="702" alt="Packet_Primer_1" src="https://github.com/sahinyurek/picoCTF-writeups/assets/62119201/61562309-ad7a-41d7-87af-b578285ea996">

Filter out with !arp
First 3 lines are TCP handshake. See the PSH flag it means it has data.

<img width="701" alt="Packet_Primer_2" src="https://github.com/sahinyurek/picoCTF-writeups/assets/62119201/8fa03adb-0950-4f8c-b1c1-e0efefb11a85">
