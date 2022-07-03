Viewing Ethernet Controller Statistics - CSMA/CD check
S2# show controllers ethernet-controller FastEthernet 0/1

ex) 
Transmit FastEthernet0/1
12887370 Bytes
24442 Unicast frames
1118 Broadcast frames
0 Discarded frames
0 Too old frames
0 Deferred frames
0 1 collision frames
0 2 collision frames
(...)
0 15 collision frames
0 Excessive collisions
0 Late collsions
0 Good (1 coll) frames
0 Good (>1 coll) frames
0 Pause frames
0 VLAN discard frames
0 Excess defer frames
0 Too large frames
154827 64 byte frames
8156 127 byte frames
0 255 byte frames
4076 511 byte frames
1020 1023 byte frames
0 1518 bye frames

from the ex resault above.
defer frames : This content indicates the number of frames that have been transmitted after waiting because another device is transmitting frames.
1 collision frames : This content indicates the number of frames that have been transmitted after 1 collision happened.
2 collision frames : This content indicates the number of frames that have been transmitted after 2 collision happened.
excessive collisions : Excessive collisions indicate the number of frames that could not be transmitted in the end because the number of impulses in the same frame exceeded 15.
