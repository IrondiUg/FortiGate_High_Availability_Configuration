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
