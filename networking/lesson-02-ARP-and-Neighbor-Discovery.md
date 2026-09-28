# lesson 02 - ARP and Neighbor Discovery

## Objective

Learn how devices on the same local Area Network (LAN) discover reach other's MAC addresses before sending Ethernet frames.

---

## Concerpts Learned

- Difference between an IP address and MAC address
- What ARP (Address Resolution Protocol) does
- Why devices need MAC addresses on a LAN
- How linux stores neighbor information
- Understanding REACHABLE, STALE, AND FAILED neighbor states

---

## Commands used 

### View the ARP Cache

'''bash
arp -a
'''

### View the neighbor Table

'''bash
arp -a
'''

### Delete a Neighbor Table

'''bash
ip neigh
'''

### Delete a Neighbor Entry

'''bash
sudo ip neigh del 192.168.1.1 dev ens18
'''

### Ping the default gateway 

'''bash
ping -c 2 192.168.1.1

### Verify the Neighbor Table Again

'''bash
ip neigh
'''

---

## What Heppened

1. Dispalyed the current ARP cache.
2. Viewed the Linux neighbor table using 'ip neigh'.
3. Delete the APR entry for the default gateway.
4. Sent a ping to the gatway.
5. Linux automatically learned the gatway's MAC address again.
6. Verified the neighbor state changeed back to **REACHABLE**.

---

## Neighbor States

| State | meaning |
|--------|----------|
| REACHABLE | Linux recently communicated with the device. |
| STALE | The MAC address is known but has not been used recently. |
| FAILED | Linux could not resolve the MAC address. |

---

## key Takeaways

- Devices communicate on an Ethernet network using **MAC addresses**, not IP addresses.
- ARP maps an IP address to its corresponding MAC address.
- linux stores this information in the neighbor table.
- If an entry is removed, linux automatically learns it again when communiction resumes.
- devices on the same LAN communicates directly after learning each other's MAC addresses.

---

## Commands Summary

'''bash
arp -a
ip neigh
sudo ip neigh del 192.168.1.1 dev ens18
ping -c 2 192.168.1.1
ip neigh
