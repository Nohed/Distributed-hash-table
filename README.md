# :file_cabinet: Distributed-hash-table :file_cabinet:
Me and c22vli@cs.umu.se together created a distributed hash table in C.
The hash table stores a persons **Social Security Number**, **Name**, **Email**. :card_index_dividers:

## Description

### Key Features

 - Dynamic Network Participation: Nodes can join an existing network or 
  start a new one if they're the first node.
  
- Range-Based Key Distribution: Each node is responsible for a specific range of the hash space (from 0-255).

- Graceful Network Management: When nodes join or leave, the network automatically redistributes key ranges and data.
  
- Fault Tolerance: The network maintains integrity even as nodes come and go.

### Communication
Uses **PDU´s** defined [here](resources/pdu.h).
Uses
- [x] TCP
- [x] UDP
For communications between nodes. And for interacting with the network.

### Usage
    ./c_node <tracker_address> <tracker_port>
#### Starting nodes**

<img width="800" alt="Screenshot 2025-03-10 at 23 08 23" src="https://github.com/user-attachments/assets/84a81820-534e-445a-9324-edee1c92ecea" />

#### With data

<img width="800" alt="Screenshot 2025-03-10 at 23 09 00" src="https://github.com/user-attachments/assets/39b6eba8-b942-4775-a123-d0b48ecdacc7" />

## limitation
Current hash range is 255, therefore the distrubuted table can only store 255 unique SSD´s.

