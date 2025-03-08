# Cisco Networking Notes

## **Basic Commands**

### **Hostname Configuration**

```cisco
hostname
banner motd ##
```

### **Enable and Line Passwords**

```cisco
enable secret [pass]
line con 0
password [pass]
login
line vty 0 15  # 0-15 for switches, 0-4 for routers
password [pass]
login
enable password [pass]
service password-encryption
```

---

## **Static Routing**

```cisco
ip route 0.0.0.0 0.0.0.0 serial 0/0/0
```

---

## **Routing Protocols**

### **RIP (Routing Information Protocol)**

- Uses a **maximum of 16 hops**

```cisco
router rip
network 10.0.0.0
network 11.0.0.0
```

### **EIGRP (Enhanced Interior Gateway Routing Protocol)**

```cisco
# View neighbor table
> show ip eigrp neighbor

# Configure EIGRP
router eigrp [AS#]  # AS (Autonomous System) number: 1-65535
network 10.0.0.0 [Wildmask]
network 11.0.0.0 [Wildmask]  # Wildmask = 255.255.255.255 - subnet mask
```

---

## **OSPF (Open Shortest Path First)**

### **OSPF Notes**

- **Link-state routing protocol**
- **Hello packets** sent every **10 seconds** (4 times)

```cisco
# View OSPF information
> show ip ospf neighbor   # View neighbor table
> show ip ospf database   # View link-state database

# OSPF Configuration
> ip ospf priority [value]   # 0-255 (highest value becomes DR)
> clear ip ospf process      # Reset all OSPF processes

# OSPF Cost Calculation
> ip ospf cost
  auto-cost reference-bandwidth
```

### **OSPFv2 (IPv4)**

#### **Single Area OSPF**

```cisco
router ospf [PID]    # PID: 1-65535
router-id [RID]      # Example: 1.1.1.1 (Highest RID is the Designated Router)
network 10.0.0.0 [WM] area [area-id]  # Area ID = 0 for a single area
```

#### **Multiaccess OSPF**

- **Multicast IPv4 Address**: `224.0.0.5`
- **Multiaccess Address**: `224.0.0.6`

---

## **IP Address Classification**

| Class       | Subnet Mask   | Networks             | Devices    | Borrow | Notes                                                                    |
| ----------- | ------------- | -------------------- | ---------- | ------ | ------------------------------------------------------------------------ |
| A           | 255.0.0.0     | 126                  | 16 million | 22     | All `0s` are host portion, others (excluding first) are network portions |
| B           | 255.255.0.0   | 16k                  | 65k        | 14     |                                                                          |
| C           | 255.255.255.0 | 2 million            | 254        | 6      |                                                                          |
| **Special** | 127           | **Loopback Address** |            |        |                                                                          |

📌 **More details**: [Cisco Learning Network](https://learningnetwork.cisco.com/s/question/0D53i00000Kt4O3CAJ/class-a-b-c)

