---
title: "DADTKV"
excerpt: "DADTKV is a distributed transactional key-value store developed as part Distributed Systems course of the Master's programs in Computer Science at Instituto Superior Técnico."
header:
  image: /assets/images/pexels-cookiecutter-17323801.jpg
  teaser: assets/images/pexels-cookiecutter-17323801.jpg
sidebar:
  - title: "Responsibilities"
    text: "Developer, Designer"
---
## 1. Introduction
The project aims to design and implement DADTKV, a distributed transactional key-value store. It's developed as part of the Master's programs in Computer Science at Instituto Superior Técnico. DADTKV facilitates the management of data objects residing in server memory, allowing concurrent access by transactional programs running on different machines.
{: style="text-align: justify;"}

## 2. Architecture
### 2.1. Components:
- **Clients:** Execute transactions on data stored in the DADTKV system.
- **Transaction Managers (TM):** Provide transactional access to stored data and replicate transaction updates across the system.
- **Lease Manager Servers (LM):** Regulate concurrent access to shared data by providing leases to transaction managers. Leases are acquired through a consensus algorithm executed among lease manager servers.
{: style="text-align: justify;"}

### 2.2. Data Model:
- Data objects are represented as <key, value> pairs.
- Each shared object can only be accessed within a valid transaction.
- Transactions consist of sets of read and write operations, ensuring strict serializability.
{: style="text-align: justify;"}

## 3. DADTKV Client Library
The DADTKV client library provides a set of methods for clients to interact with the DADTKV system:
- `List<DadInt> TxSubmit(string clientId, List<string> readSet, List<DadInt> writeSet):` Submits a transaction for execution, specifying the client ID, the set of DadInts to be read, and the set of DadInts to be written.
- `bool Status():` Outputs the current state of all nodes in the system.
{: style="text-align: justify;"}

## 4. Implementation
DADTKV is implemented using C# and gRPC for remote communication. Key features of the implementation include:
- **Fault Tolerance:** Mechanisms are in place to ensure system resilience, allowing the system to continue making progress even if a minority of servers fail.
- **Time Slots:** The system's state is updated in a sequence of time slots, allowing for fault tolerance testing and system monitoring.
{: style="text-align: justify;"}

## 5. Documentation
- The final report can be found [here](/assets/documents/DAD_Project_Report.pdf);
- The original paper on the Paxos consensus algorithm can be found [here](https://lamport.azurewebsites.net/pubs/paxos-simple.pdf).
{: style="text-align: justify;"}

[See on github](https://github.com/MiguelRocha2001/IST-DAD-DADTKV){: .btn .btn--info}