# Network Security Concepts and Technologies

---

## 1. IDS vs IPS

- **IDS (Intrusion Detection System):** Monitors network or system activities for malicious activities or policy violations.
- **IPS (Intrusion Prevention System):** Monitors, detects, and actively prevents or blocks intrusions.

---

## 2. Types of IDS/IPS

### A. Network-based IDS/IPS (NIDS/NIPS)
- Monitors network traffic for all devices on the network.

### B. Host-based IDS/IPS (HIDS/HIPS)
- Monitors activities on a single host or device.

---

## 3. Types of Alerts

- **True Positive:** Attack is correctly detected.
- **True Negative:** No attack and system correctly ignores.
- **False Positive:** Legitimate activity incorrectly flagged as attack.
- **False Negative:** Attack is missed/not detected.

---

## 4. Firewall and Its Architecture

### A. Bastion Hosts
- Hardened server designed to withstand attacks.

### B. Screened Subnet (DMZ)
- A network segment isolated for public-facing services, separated from internal network.

### C. Multi-homed Firewall
- Firewall with multiple network interfaces to connect separate networks (e.g., internal, external, DMZ).

---

## 5. Types of Firewalls

### A. Configuration-based

- **Network-based Firewall:** Protects entire networks.
- **Host-based Firewall:** Protects individual hosts.

### B. Working Principle-based

- **Packet Filtering Firewall:** Filters packets based on header information (IP, port, protocol).
- **Circuit-level Gateway:** Monitors TCP handshakes and sessions.
- **Application-level Gateway (Proxy Firewall):** Inspects and filters at the application layer.
- **Stateful Multilayer Inspection:** Tracks state of active connections and makes decisions based on context.

- **Application Proxy:** Acts as an intermediary for requests from clients seeking resources.

---

## 6. VPN (Virtual Private Network)

- Technology that creates a secure, encrypted connection over a less secure network (e.g., the Internet).

---

## 7. FireWalking

- Technique to determine firewall rule sets by sending probes with varying TTL values.

---

## 8. Tunneling Techniques

- **ICMP Tunneling:** Encapsulates data in ICMP packets to bypass firewalls.
- **ACK Tunneling:** Uses TCP ACK packets to tunnel data.
- **HTTP Tunneling:** Encapsulates data within HTTP packets.
- **SSH Tunneling:** Uses SSH protocol to securely tunnel data.
- **DNS Tunneling:** Encapsulates data within DNS queries and responses.

---

## 9. DTP (Dynamic Trunking Protocol)

- Cisco proprietary protocol used to negotiate trunking on a link between two switches.

---

## 10. Honeypots and Its Types

- **Honeypot:** Decoy system intended to attract cyber attackers and study their techniques.

### Types of Honeypots:

- **Production Honeypots:** Used in companies to detect or deflect attacks.
- **Research Honeypots:** Used by researchers to study attacker behavior.
