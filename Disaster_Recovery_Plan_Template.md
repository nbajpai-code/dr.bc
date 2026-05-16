# Disaster Recovery Plan (DRP) Template

This document provides a structured template for creating a comprehensive Disaster Recovery Plan. It should be populated with specific details derived from the Business Impact Analysis (BIA) and tailored to the organization's architecture.

## 1. Introduction and Scope
* **Purpose:** The purpose of this DRP is to provide procedures for recovering critical IT infrastructure and services following a disruption.
* **Scope:** This plan covers the systems, networks, and applications located at [Primary Data Center/Cloud Region]. It does *not* cover [Exclusions, e.g., endpoint devices].
* **Assumptions:** List assumptions (e.g., key personnel will be available, secondary site is operational).

## 2. Roles and Responsibilities
Define the Disaster Recovery Team (DRT).
* **DR Coordinator / Incident Commander:** Overall authority during a disaster.
* **Infrastructure Team Lead:** Responsible for network, servers, and storage recovery.
* **Application Team Lead:** Responsible for restoring applications and databases.
* **Communications Lead:** Responsible for internal and external messaging.

*Include a contact list with primary and secondary contact methods (phone, email, emergency notification system).*

## 3. Incident Response and Declaration
* **Incident Detection:** How are disruptions detected and reported?
* **Assessment:** How is the severity of the incident assessed?
* **Declaration Criteria:** Who has the authority to officially declare a "Disaster" and invoke the DRP? Under what conditions?

## 4. Recovery Procedures (Phase 1: Activation)
* **Initial Actions:** Steps to take immediately upon declaration.
* **Team Assembly:** Where and how the DR team convenes (physical war room or virtual bridge).
* **Damage Assessment:** Procedures for determining the extent of the damage to primary systems.

## 5. Recovery Procedures (Phase 2: Execution)
*This section contains the step-by-step technical runbooks for recovery. Prioritize based on BIA tiers.*

### Tier 1: Mission Critical Systems (RTO < 4 Hours)
* **System A (e.g., Identity Provider / Active Directory)**
    * Prerequisites
    * Recovery Steps
    * Verification Steps
* **System B (e.g., Core Database)**
    * Prerequisites
    * Recovery Steps (e.g., failover to replica, restore from snapshot)
    * Verification Steps

### Tier 2: Important Systems (RTO 24 Hours)
* **System C**...

### Tier 3: Deferrable Systems (RTO > 3 Days)
* **System D**...

## 6. Recovery Procedures (Phase 3: Reconstitution/Failback)
* **Failback Planning:** How and when to return operations to the primary site once it is restored.
* **Data Synchronization:** Ensuring data generated at the DR site is synced back to the primary site without loss.
* **Verification:** Final testing to ensure the primary site is fully operational.
* **Stand Down:** Officially ending the disaster state.

## 7. Plan Maintenance and Testing
* **Maintenance Schedule:** The DRP must be reviewed and updated [Annually/Bi-annually] or upon major infrastructure changes.
* **Testing Schedule:** The DRP must be tested [Quarterly/Annually].
* **Training:** DR team members must receive annual training on their roles.

---
## Appendix A: Network Diagrams
*Insert or link to current network diagrams showing primary and DR topologies.*

## Appendix B: Vendor Contact List
*List of critical vendors (ISPs, Cloud Providers, Hardware Vendors) with SLA details and contact information.*
