## FortiGate High Availability (HA) Lab

This lab demonstrates the configuration and verification of FortiGate High Availability (HA) using an Active-Passive deployment.

**The objective** is to build a redundant firewall setup where one FortiGate operates as the Primary (Active) unit while the second FortiGate remains in a Secondary (Passive) state and is ready to take over if the active unit becomes unavailable.

### Lab Objectives
- Configure two FortiGate firewalls for High Availability.
- Deploy the FortiGates in Active-Passive mode.
- Configure HA parameters and cluster communication.
- Verify HA synchronization between the two firewalls.
- Identify the primary and secondary units.
- Simulate a firewall failure.
- Verify automatic failover.
- Confirm that the secondary unit takes over as the new primary.
- Understand the role of HA in improving firewall availability and reducing downtime.

### HA Mode: Active-Passive
**Active Unit**:  The active FortiGate is responsible for handling production traffic and forwarding packets between the relevant interfaces/networks.

**Passive Unit**:  The passive FortiGate continuously monitors the HA cluster and remains ready to assume the active role if the primary unit becomes unavailable.

**Under normal operation:**
- FortiGate 01 → PRIMARY / ACTIVE
- FortiGate 02 → SECONDARY / PASSIVE

**If the active unit fails:**
- FortiGate 01 → OFFLINE
- FortiGate 02 → PRIMARY / ACTIVE

This allows the firewall service to continue with minimal interruption.

## HA Heartbeat / Cluster Communication
The HA heartbeat interfaces allow the FortiGates to communicate with each other and exchange cluster information.
The heartbeat connection is important because the FortiGates use it to determine whether the other cluster member is still available.
Conceptually:
FortiGate 01
     |
     | HA Heartbeat
     |
FortiGate 02

The heartbeat connection allows the cluster members to monitor each other's state.
