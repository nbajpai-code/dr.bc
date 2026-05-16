# RTO and RPO Strategies

Recovery Time Objective (RTO) and Recovery Point Objective (RPO) are the two most critical metrics in Disaster Recovery. They dictate the architecture, technology choices, and cost of your DR solution.

## Defining the Metrics

* **RTO (Recovery Time Objective):** The duration of time within which a business process must be restored after a disruption to avoid unacceptable consequences. It answers the question: *"How long can we afford to be down?"*
* **RPO (Recovery Point Objective):** The maximum tolerable period in which data might be lost. It dictates the frequency of backups or replication. It answers the question: *"How much data can we afford to lose?"*

---

## RPO Strategies (Data Protection)

The lower the RPO (closer to zero data loss), the more expensive and complex the solution.

### 1. RPO of 24 Hours (Tape/Disk Backup)
* **Strategy:** Nightly backups.
* **Technology:** Traditional backup software to local disk, then vaulted to offsite storage or cloud storage (e.g., AWS S3 Glacier).
* **Pros:** Low cost, simple.
* **Cons:** Up to 24 hours of data loss.

### 2. RPO of 1-4 Hours (Snapshotting / Frequent Backups)
* **Strategy:** Incremental backups or storage snapshots taken throughout the day.
* **Technology:** SAN snapshots, Cloud provider volume snapshots (e.g., EBS snapshots), continuous data protection (CDP) software configured for frequent intervals.
* **Pros:** Balances cost and data protection.
* **Cons:** Still involves some data loss; performance impact during snapshot creation.

### 3. RPO of Near-Zero (Asynchronous Replication)
* **Strategy:** Data is replicated to a secondary site continuously, but the primary transaction doesn't wait for acknowledgment from the secondary site.
* **Technology:** Storage-level replication (e.g., SRDF/A), database log shipping (e.g., SQL Server AlwaysOn async), cloud replication tools (e.g., AWS Elastic Disaster Recovery).
* **Pros:** Minimal data loss (usually seconds or minutes), no impact on primary site performance.
* **Cons:** Higher bandwidth requirements, requires secondary storage infrastructure.

### 4. RPO of Zero (Synchronous Replication)
* **Strategy:** Every write to the primary storage must be acknowledged by the secondary storage before the transaction completes.
* **Technology:** Metro-clusters, storage synchronous replication (e.g., SRDF/S), multi-AZ database clustering.
* **Pros:** Zero data loss. Guaranteed consistency.
* **Cons:** Highly sensitive to latency. Usually limited to short distances (e.g., < 100km). Highest cost.

---

## RTO Strategies (System Recovery)

Like RPO, the lower the RTO (faster recovery), the more expensive the solution.

### 1. Cold Site (RTO: Days to Weeks)
* **Strategy:** An empty facility with power and cooling, but no hardware installed.
* **Process:** During a disaster, hardware must be procured, shipped, installed, configured, and data restored from backup.
* **Pros:** Very low ongoing cost.
* **Cons:** Extremely slow recovery.

### 2. Warm Site (RTO: Hours to Days)
* **Strategy:** A facility with hardware installed and networked, but systems may not be fully configured, and data is not continuously synced.
* **Process:** During a disaster, the latest data is restored from backup, and systems are reconfigured and brought online.
* **Pros:** Balance of cost and recovery speed.
* **Cons:** Manual intervention required to spin up services.

### 3. Hot Site / Pilot Light (RTO: Minutes to Hours)
* **Strategy:** Core infrastructure runs continuously at the secondary site. Critical data is replicated.
* **Process:** During a disaster, additional compute resources are scaled up, and DNS/Traffic is cut over.
* **Pros:** Fast recovery.
* **Cons:** Higher cost due to maintaining running infrastructure.

### 4. Active-Active / Multi-Region (RTO: Near Zero)
* **Strategy:** Application is deployed identically across two or more separate sites/regions. Traffic is load-balanced between them.
* **Process:** If one site fails, traffic is automatically routed to the remaining active site(s).
* **Pros:** Zero or near-zero downtime. Seamless failover.
* **Cons:** Highest complexity and cost. Requires active-active database architectures and stateless application design.
