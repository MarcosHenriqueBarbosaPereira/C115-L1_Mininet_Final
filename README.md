
# C115-L1_Mininet_Final
Repository for my final homework for Mininet tool for C115 subject.

## Contents

- [Activity 1](#activity-1)
  - [1- Login in to Mininet Virtual Machine through PuTTy](#1--login-in-to-mininet-virtual-machine-through-putty)
  - [2- Creating the Topology](#2--creating-the-topology)
  - [3- Inspecting Topology Information](#3--inspecting-topology-information)
    - [Topology Nodes](#topology-nodes)
    - [Topology Net](#topology-net)
    - [Logical Ports Addresses](#logical-ports-addresses)
    - [Hosts Data](#hosts-data)
    - [Topology Image](#topology-image)
  - [4- Ping Test for all Nodes](#4--ping-test-for-all-nodes)
  - [5- Server-Client Test](#5--server-client-test)
    - [Setting Host1 as Server and Host2 as Client](#setting-host1-as-server-and-host2-as-client)
    - [Host-Client 1Mbps](#host-client-1mbps)
    - [Host-Client 5Mbps](#host-client-5mbps)
    - [Host-Client 10Mbps](#host-client-10mbps)
    - [Host-Client 15Mbps](#host-client-15mbps)
    - [Host-Client 20Mbps](#host-client-20mbps)
    - [Host-Client 25Mbps](#host-client-25mbps)
- [Activity 2](#activity-2)
  - [1- Custom Topology Code](1--custom-topology-code)
  - [2- Creating the Custom Topology](#2--creating-the-custom-topology)
  - [3- Inspecting Custom Topology Information](#3--inspecting-custom-topology-information)
    - [Custom Topology Nodes](#custom-topology-nodes)
    - [Custom Topology Net](#custom-topology-net)
    - [Custom Logical Ports Addresses](#custom-logical-ports-addresses)
    - [Custom Hosts Data](#custom-hosts-data)
    - [Custom Topology Image](#custom-topology-image)
  - [4- Ping Test for all Custom Nodes](#4--ping-test-for-all-custom-nodes)
  - [5- Recreating Rules](#5--recreating-rules)
    - [Deleting Existing Rules](#deleting-existing-rules)
    - [Creating Rules for h1-h4 Communication](#creating-rules-for-h1-h4-communication)
  - [6- Ping Test for New Rules](#6--ping-test-for-new-rules)
- [About](#about)

---

## Activity 1

### Proposal

The following text describes the proposal for this activity:

```text
Consider a linear topology with eight hosts.
  - Use Mininet's standard command line to create the topology with standardized MAC addresses, bandwidth of 30 Mbps, and Mininet's default controller.
  - Inspect the interfaces, MAC, IP, and port addresses via command-line tools.
  - Perform ping tests between all nodes, capturing packets with `tcpdump`.
  - Host 1 on port 5555 will be a TCP server, and Host 2 a client. Run iperf tests for bandwidths of 1.5, 10, 15, 20, and 25 Mbps, with reports generated every second for 15 seconds.
```

### 1- Login in to Mininet Virtual Machine through PuTTy

![Putty Connection](images/putty/putty-connection.png)
![Login to Mininet Virtual Machine through PuTTy](images/putty/login.png)

---

### 2- Creating the Topology

![Creating the Topology](images/putty/creating-topology.png)

---

### 3- Inspecting Topology Information

#### Topology Nodes

![Topology Nodes](images/putty/nodes.png)

---

#### Topology Net

![Topology Net](images/putty/net.png)

---

#### Logical Ports Addresses

![Logical Ports Addresses](images/putty/dump.png)

---

#### Hosts Data

![Hosts Info h1-h2](images/putty/ifconfig-h1-h2.png)
![Hosts Info h3-h4](images/putty/ifconfig-h3-h4.png)
![Hosts Info h5-h6](images/putty/ifconfig-h5-h6.png)
![Hosts Info h7-h8](images/putty/ifconfig-h7-h8.png)

---

#### Topology Image

![Topology Miniedit Image](images/miniedit/topology-image.png)

---

### 4- Ping Test for all Nodes

![PingAll Test](images/putty/pingall.png)

---

### 5- Server-Client Test

#### Setting Host1 as Server and Host2 as Client

![H1 Server and H2 Client](images/xterm/iperf-30M.png)

---

#### Host-Client 1Mbps

![H1 Server and H2 Client](images/xterm/iperf-1M.png)

---

#### Host-Client 5Mbps

![H1 Server and H2 Client](images/xterm/iperf-5M.png)

---

#### Host-Client 10Mbps

![H1 Server and H2 Client](images/xterm/iperf-10M.png)

---

#### Host-Client 15Mbps

![H1 Server and H2 Client](images/xterm/iperf-15M.png)

---

#### Host-Client 20Mbps

![H1 Server and H2 Client](images/xterm/iperf-20M.png)

---


#### Host-Client 25Mbps

![H1 Server and H2 Client](images/xterm/iperf-25M.png)

---

## Activity 2

### Proposal

The following text describes the proposal for this activity:

```text
Consider a custom topology with multiple hosts and switches:
  - Use Mininet's standard command line to create the topology with standardized MAC addresses and a manual controller configuration.
  - Inspect the interfaces, MAC, IP, and port addresses via command-line tools.
  - Create a visual representation of the topology, including all information obtained in the inspection step.
  - Perform ping tests between all nodes using normal switch configurations to verify connectivity.
  - Delete the existing flow rules and create new rules based on MAC addresses for specific nodes, ensuring communication between hosts connected to different switches.
  - Perform ping tests to demonstrate that the new MAC-based rules were successfully implemented.
```

![Reference Image for the Topology](images/miniedit-python/topology-image.png)

---

### 1- Custom Topology Code

The following code can be found in this project, located in [custom_topo.py](python/custom_topo.py).

![Custom Topology Code](images/putty-python/custom-topo-code.png)

---

### 2- Creating the Custom Topology

![Creating the Custom Topology](images/putty-python/creating-topology.png)

---

### 3- Inspecting Custom Topology Information

#### Custom Topology Nodes

![Custom Topology Nodes](images/putty-python/nodes.png)

---

#### Custom Topology Net

![Custom Topology Net](images/putty-python/net.png)

---

#### Custom Logical Ports Addresses

![Custom Logical Ports Addresses](images/putty-python/dump.png)

---

#### Custom Hosts Data

![Custom Hosts Info h1-h2-h3](images/putty-python/ifconfig-h1-h2-h3.png)
![Custom Hosts Info h4-h5](images/putty-python/ifconfig-h4-h5.png)
![Custom Hosts Info h6-h7](images/putty-python/ifconfig-h6-h7.png)

---

#### Custom Topology Image

![Custom Topology Spear Image](images/spear/topology-image.png)

---

### 4- Ping Test for all Custom Nodes

![PingAll Test for Custom Nodes](images/putty-python/pingall.png)

---

### 5- Recreating Rules

#### Deleting Existing Rules

![Deleted Rules](images/xterm-python/deleted-rules.png)

---

#### Creating Rules for h1-h4 Communication

![Rules h1-h4](images/xterm-python/rules-h1-h4.png)

---

### 6- Ping Test for New Rules

![Ping h1-h4 new rules](images/xterm-python/ping-h1-h4.png)

---

## About

This repository is part of my learning journey using Mininet for network simulation tasks in the C115 course.
