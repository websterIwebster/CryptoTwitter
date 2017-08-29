# Distributed systems and Byzantine nodes

A blockchain is a distributed, or a decentralized distributed, system, and in order to understand blockchains, it’s essential first to understand these distributed systems.

### What is a decentralized distributed system?

A centralized system is a system in which both the state of your system and the program itself are stored on a single computer. For example, if you download a PDF document your boss sent you, your computer crashes, and you don’t have a backup, then you are out of luck.

However, if you were using a distributed system to store the PDF, such as Google Drive or Dropbox, you can download that document on another computer, because Google Drive and Dropbox store your files ‘in the cloud,’ meaning they are stored across multiple machines. Using multiple machines to store, in this example, a PDF, makes the process fault-tolerant—the state is divided over multiple servers/computers. So it doesn’t matter if one of Dropbox’s servers fail, because it’s replicated across their other machines. 

Distributed systems is a computing paradigm that refers to using two or more machines that work with each other. However, these decentralized systems are complex, and are considered an advanced topic in computer science. 

A node is defined as a single server/computer/player in a distributed system. All nodes in a distributed system should be able to send and receive messages from each other. However, nodes can also be faulty or malicious, and the unexpected behavior of a node on the network is part of the Byzantine problem.

In a distributed design, coordination between nodes and fault tolerance a challenge. If some nodes become faulty or their connections break, the distributed system should be able to tolerate this and continue to work without an error to get the desired result (For example, think of when you run your Bitcoin Core wallet or any other altcoin core wallet—you should still be able to sync, despite faulty nodes on the network).

### Byzantine

How can you design a system to survive the worst possible failures? Let's say a node in your system is a “traitor node,” that it sends one answer to one node, and a totally different answer to another node; this can lead the distributed system to try to perform an incorrect answer. This could happen, if, for example, a node generates a null response, runs out of memory, or is owned by a deliberate attacker/hacker. This may lead to a Byzantine failure.

Bitcoin is the perfect example, since your computer should not trust every other node/peer in the network—it would be pretty bad if one node had problems and took down the entire Bitcoin network. Another example is flight systems, like in a Boeing 777 or 787. A hardware failure might exhibit Byzantine-like behaviors, so they have build a byzantine fault-tolerant flight control system into these aircrafts.

### CAP Theorem

Distributed systems can not have Consistency, Availability, and Partition Tolerance simultaneously.

- Consistency: ensures all nodes in a distributed system have the latest copy.

- Availability: ensures the system is up, accessible, accepting incoming requests, and responding when required and without any failures.

- Partition: ensures that if a group of nodes fails, the distributed system will continue to operate correctly.  

A typical distributed system can not have all of these properties at the same time, yet the Blockchain somehow can.

The use of replication achieves fault tolerance. Consistency is achieved by using consensus algorithms to ensure that all nodes have the same data—this is also called State Machine Replication. The blockchain is sort of a method to achieve State Machine Replication.

The Byzantine Generals Problem (https://en.wikipedia.org/wiki/Byzantine_fault_tolerance#Byzantine_Generals.27_Problem) was solved in 1999, and in 2009 the first implementation was made together with Bitcoin, where a PoW (Proof Of Work) algorithm was developed as a mechanism to achieve consensus.

Consensus is a process of agreement between distrusting nodes on a final state of data. In order to achieve consensus, different algorithms can be used. The concept of multiple nodes (for example, hundreds or thousands of nodes) is known as a distributed consensus.
