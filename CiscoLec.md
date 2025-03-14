# ENSA Module 1: Single-Area OSPFv2 Concepts - Reviewer

## Module Objectives
- Explain how single-area OSPF operates in both **point-to-point** and **broadcast multiaccess** networks.

## 1.1 OSPF Features and Characteristics
### **Introduction to OSPF**
- OSPF (Open Shortest Path First) is a **link-state routing protocol**.
- Developed as an alternative to **Routing Information Protocol (RIP)**.
- **Advantages over RIP:**
  - Faster convergence
  - Scales to larger networks
  - Uses concept of areas to manage routing updates.
- OSPF uses **link-state information**.
  - A **link** is an interface on a router, a network segment that connects routers, or a stub network.
  - Information about a link is known as a **link-state**.

### **Components of OSPF**
- OSPF uses **routing protocol messages** to exchange route information.
- OSPF exchanges **five types of packets**:
  1. **Hello Packet**
 2. **Database Description (DBD) Packet**
 3. **Link-State Request (LSR) Packet**
 4. **Link-State Update (LSU) Packet**
 5. **Link-State Acknowledgment (LSAck) Packet**
- OSPF maintains **three databases**:
  1. **Neighbor Table (Adjacency Database)** – Stores details of OSPF neighbors.
  2. **Link-State Database (LSDB)** – Contains the network topology.
 3. **Routing Table (Forwarding Table)** – Built using the **Dijkstra SPF Algorithm**.
- **Link-State Routing Process**
  - **Steps to Convergence:**
    1. **Establish Neighbor Adjacencies**
 2. **Exchange Link-State Information**
 3. **Build the Link-State Database (LSDB)**
 4. **Run the SPF Algorithm**
 5. **Choose the Best Route**

### **Single-Area and Multiarea OSPF**
- **Single-Area OSPF:**
  - Used for smaller networks.
  - All routers share the same link-state database.
  
- **Multiarea OSPF:**
  - Uses **hierarchical routing** with multiple areas.
  - All areas must connect to the backbone **Area 0**.
  - **Area Border Routers (ABRs)** connect multiple areas.
  - Advantages:
    - **Smaller routing tables** – Due to summarized network addresses.
    - **Reduced SPF calculations** – Limits topology changes within a single area.
    - **Reduced processing & memory usage** – Improves efficiency.

## 1.2 OSPF Packets
- **Five OSPFv2 Packet Types:**
  1. **Hello** – Establishes neighbor relationships.
 2. **Database Description (DBD) Packet** – Summarizes database contents.
 3. **Link-State Request (LSR) Packet** – Requests specific information from neighbors.
 4. **Link-State Update (LSU) Packet** – Sends requested topology information.
 5. **Link-State Acknowledgment (LSAck) Packet** – Acknowledges receipt of LSUs.
- **OSPF Hello Packet Functions:**
  - Discover neighbors & establish adjacencies.
  - Maintain neighbor relationships.
  - Determine Designated Router (DR) and Backup DR (BDR) in multiaccess networks.
  - Sent to IPv4 multicast address **224.0.0.5** (OSPFv2).

## 1.3 OSPF Operation
### **OSPF Neighbor Adjacency Formation**
- **OSPF Neighbor States:**
  1. **Down** – No received Hello packets.
 2. **Init** – Router has received a Hello but no 2-way communication yet.
 3. **Two-Way** – Both routers have received Hello packets and formed a neighbor relationship.
 4. **ExStart** – Master/slave election occurs for database exchange.
 5. **Exchange** – Routers exchange DBD packets containing LSDB information.
 6. **Loading** – Routers request missing LSAs with LSR packets.
 7. **Full** – Routers are synchronized and have completed the adjacency process.

### **Single-Area OSPF Process**
1. Establish **neighbor adjacencies** via Hello packets.
2. Exchange **link-state information** with neighbors.
3. Build the **Link-State Database (LSDB)**.
4. Run the **Shortest Path First (SPF) algorithm**.
5. Choose **best routes** and populate the routing table.

### **The Need for a Designated Router (DR) in Multiaccess Networks**
- Multiaccess networks create too many **adjacencies**.
- Too many LSAs cause excessive flooding, impacting network performance.
- **Designated Router (DR)**: Central router that manages LSA flooding.
- **Backup Designated Router (BDR)**: Backup in case DR fails.
- **DROTHERs**: Other OSPF routers that do not become DR or BDR.

## **Key Takeaways**
- **OSPF** is a **link-state routing protocol**, an alternative to RIP.
- Uses the **Dijkstra SPF Algorithm** to calculate shortest paths.
- OSPF messages include: **Hello, DBD, LSR, LSU, and LSAck**.
- OSPF uses **Single-Area** and **Multiarea** designs.
- In **Multiaccess networks**, OSPF elects a **Designated Router (DR)** to reduce LSA flooding.
- **OSPFv3** supports **IPv6** and uses similar operations to OSPFv2.

## **Additional Learning Activities**
- **Packet Tracer Physical Mode Activities** – Simulates real-world router configurations.
- **Check Your Understanding** – Self-assessment questions to reinforce learning.
- **Classroom Discussions** – Important discussion topics include:
  - Benefits of Multiarea OSPF.
  - OSPF Hello Packets & LSAs.
  - DR/BDR roles in multiaccess networks.

---

# ENSA Module 2: Single-Area OSPFv2 Configuration - Reviewer

## **Module Objectives**
- Implement single-area OSPFv2 in both **point-to-point** and **broadcast multiaccess networks**.

## **2.1 OSPF Router ID**
### **OSPF Router ID Overview**
- OSPFv2 is enabled using the `router ospf <process-id>` command.
- The **process ID** is locally significant (1 to 65,535) but should be consistent across all routers.
- The OSPF **Router ID (RID)** is a **32-bit number** formatted like an IPv4 address and is unique for each router.
- **Router ID Selection Order:**
  1. Explicitly configured via `router-id rid` command.
  2. Highest IPv4 address of any loopback interface.
 3. Highest active IPv4 address of any physical interface.

## **2.2 Configuring OSPF on Point-to-Point Networks**
### **Configuring OSPFv2 on a Router**
- Enable OSPF using:
  ```
  Router(config)# router ospf <process-id>
  R1(config-router)# network <network-address> <wildcard-mask> area <area-id>
  ```
- Use wildcard masks to define network areas.
- Best practice: Use **area 0** for single-area OSPF.

### **OSPF Passive Interface**
- **By default, OSPF sends updates on all OSPF-enabled interfaces.**
- Use the `passive-interface <interface>` command to stop OSPF updates from being sent through an interface while still advertising that network.
- Benefits of `passive-interface`:
  - **Bandwidth efficiency** – Reduces unnecessary OSPF traffic.
  - **Security** – Prevents OSPF message interception.
  
## **2.3 Multiaccess OSPF Networks**
- Multiaccess networks use a **Designated Router (DR)** and **Backup Designated Router (BDR)** to minimize LSA flooding.
- **DR Election Process**
  - The router with the highest **priority** is elected as **DR**.
  - The router with the **second-highest priority** becomes the **BDR**.
  - **Priority range:** 0 – 255 (Default is **1**). Setting priority **0** prevents a router from being elected DR/BDR.
  - If a new router with a higher priority joins, it **does not preempt** the existing DR/BDR.

## **2.4 Modifying Single-Area OSPFv2**
### **OSPF Cost Metric**
- **OSPF uses cost as a metric** to determine the best path.
- Formula: 
  ```
  Cost = Reference Bandwidth / Interface Bandwidth
  ```
  - Default Reference Bandwidth = **100,000,000 bps (100 Mbps)**.
  - **Higher bandwidth → Lower cost**.
  - Adjust reference bandwidth with:
    ```
    Router(config-router)# auto-cost reference-bandwidth <Mbps>
    ```
  - Manually set OSPF cost per interface:
    ```
    Router(config-if)# ip ospf cost <value>
    ```

### **Hello and Dead Intervals**
- **Hello interval**: Default = **10 seconds** (multiaccess & point-to-point networks).
- **Dead interval**: Default = **4 × Hello interval (40 seconds)**.
- Modify OSPF intervals manually:
  ```
  Router(config-if)# ip ospf hello-interval <seconds>
  Router(config-if)# ip ospf dead-interval <seconds>
  ```

## **2.5 Default Route Propagation in OSPFv2**
- To propagate a default static route in OSPF:
  1. Configure a **default static route**:
    ```
    Router(config)# ip route 0.0.0.0 0.0.0.0 <next-hop | exit-intf>
    ```
  2. Instruct OSPF to propagate it:
    ```
    Router(config-router)# default-information originate
    ```
- Verify default route propagation with:
  ```
  Router# show ip route
  ```
  - Look for `O*E2` (OSPF-external Type 2) entry.

## **2.6 Verifying Single-Area OSPFv2**
### **Useful Commands**
- `show ip interface brief` – Verify active interfaces and IP addressing.
- `show ip route` – Check routing table.
- `show ip ospf neighbor` – Verify OSPF neighbors and adjacencies.
- `show ip protocols` – Display OSPF process ID, router ID, and interfaces participating in OSPF.
- `show ip ospf` – View OSPF process details.
- `show ip ospf interface` – Display OSPF settings per interface.
- `show ip ospf interface brief` – Quick summary of OSPF-enabled interfaces.

## **2.7 Module Practice and Quiz**
- **Packet Tracer Labs**:
  - **Single-Area OSPFv2 Configuration**
  - **Modifying OSPFv2 Settings**
  - **Default Route Propagation in OSPF**
- **Key Learning Points:**
  - OSPFv2 is configured using `router ospf <process-id>`.
  - The **router ID** is a unique 32-bit value used for router identification.
  - Use `passive-interface` to stop sending unnecessary OSPF updates.
  - Multiaccess networks require **DR/BDR elections** to reduce LSA flooding.
  - Adjust OSPF **cost** and **timers** to optimize routing.
  - **Default routes** can be propagated with `default-information originate`.
  - Use `show ip ospf` commands to verify OSPF configurations.

---

## **Chapter 9: Subnetting IP Networks**

### **Objectives**
- Explain why routing is necessary for hosts on different networks to communicate.
- Describe IP as a communication protocol used to identify a single device on a network.
- Explain subnetting and calculate the number of available host addresses.
- Implement subnetting based on host and network requirements.
- Describe the benefits and application of **Variable Length Subnet Masking (VLSM)**.
- Explain IPv6 address assignments in a business network.

---
## **9.1 Subnetting an IPv4 Network**

### **Why Subnetting is Important**
- **Subnetting** divides a larger network into smaller subnetworks (**subnets**).
- Benefits:
  - Controls broadcast traffic
  - Reduces overall network congestion
  - Improves performance

### **Subnetting Basics**
- **Borrowing bits** from the host portion increases the number of available subnets.
- **Formulas:**
  - **Number of Subnets** = `2^n` (where `n` is the number of borrowed bits)
  - **Number of Usable Hosts per Subnet** = `2^h - 2` (where `h` is the number of host bits)
  - Subnet **0** and the **broadcast address** cannot be assigned to hosts.

### **Examples**
- **Borrowing 1 bit**: 2 subnets
  - **Subnet 0**: `192.168.1.0 - 192.168.1.127` (Mask: `255.255.255.128`)
  - **Subnet 1**:  `192.168.1.128 - 192.168.1.255` (Mask: `255.255.255.128`)
- **Borrowing 2 bits**: 4 subnets (`2^2 = 4`)
- **Borrowing 3 bits**: 8 subnets (`2^3 = 8`)

---
## **9.2 Addressing Schemes**

### **Subnetting Based on Host Requirements**
- Consider the **number of required subnets** and **number of required host addresses**.
- **Formula for usable hosts:** `2^h - 2`

### **Subnetting Based on Network Requirements**
- Use **2^n** to determine the required number of subnets.
- Address space should be **efficiently planned** to accommodate network growth.

---
## **9.3 Variable Length Subnet Masking (VLSM)**

### **Benefits of VLSM**
- **Traditional subnetting wastes addresses** by assigning the same number of addresses to all subnets.
- **VLSM** allows subnets to have **different sizes**, optimizing IP address usage.

### **How VLSM Works**
- A network is first **subnetted**.
- Then, the subnets can be further **subnetted again** based on requirements.
- Subnet masks will **vary depending on the subnet size**.

### **Example of VLSM in Practice**
- **LANs** use a **/27 mask** (30 usable hosts per subnet).
- **WAN links** use a **/30 mask** (2 usable hosts per subnet).

---
## **9.4 IPv6 Subnetting**

### **Subnetting an IPv6 Network**
- **IPv6 subnetting** is based on the **Subnet ID**.
- Unlike IPv4, subnetting in **IPv6 is not about address conservation**, but about creating a structured design.
- **IPv6 Subnet Allocation:**
  - Subnetting occurs by using bits from the **Interface ID**.

---
## **Key Takeaways**
- **Subnetting** divides a network to improve performance and reduce congestion.
- **Subnetting formulas**:
  - `2^n` for number of subnets.
  - `2^h - 2` for number of usable hosts per subnet.
- **VLSM** allows for **more efficient** IP addressing.
- **IPv6 subnetting** is based on the **Subnet ID**, not for conserving addresses but for structuring the network.

For more details, refer to **netacad.com** or Cisco Networking Academy resources.

