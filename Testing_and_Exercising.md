# DR/BC Testing and Exercising

An untested Disaster Recovery Plan is merely a hypothesis. Regular testing is critical to identify gaps, train staff, and ensure confidence in the organization's ability to recover.

## Types of Tests

### 1. Plan Review / Desk Check
* **What it is:** A detailed review of the DRP document by the DR team and process owners.
* **Objective:** Ensure contact information is up-to-date, infrastructure changes are reflected in the plan, and basic logic holds.
* **Frequency:** Semi-annually or after major infrastructure changes.
* **Risk/Impact:** None.

### 2. Tabletop Exercise
* **What it is:** A facilitated discussion where the DR team walks through a simulated disaster scenario (e.g., Ransomware attack, physical facility fire).
* **Objective:** Validate team coordination, communication protocols, and decision-making processes. Identify procedural gaps without touching live systems.
* **Frequency:** Annually or bi-annually.
* **Risk/Impact:** None.

### 3. Simulation
* **What it is:** Similar to a tabletop, but includes mock notifications, simulated system alerts, and requires the team to locate and utilize recovery resources (e.g., accessing alternate work locations, logging into recovery systems).
* **Objective:** Test the logistics and operational readiness of the team.
* **Frequency:** Annually.
* **Risk/Impact:** Very Low.

### 4. Parallel Testing
* **What it is:** Recovering systems at the DR site and running them concurrently with the primary site. The recovered systems process historical or dummy data to verify functionality.
* **Objective:** Prove that the systems can be recovered within the RTO and that the recovered environment functions correctly.
* **Frequency:** Annually.
* **Risk/Impact:** Low to Medium. Requires careful network isolation to ensure DR systems do not interfere with primary production systems.

### 5. Full Interruption / Cutover Test
* **What it is:** The primary systems are intentionally shut down, and production traffic is routed entirely to the DR site.
* **Objective:** The ultimate test of the DR plan and infrastructure. Proves the organization can run entirely out of the DR facility.
* **Frequency:** Annually (often performed over a weekend during maintenance windows).
* **Risk/Impact:** High. If the failover fails, or failback encounters issues, actual business operations are impacted. Requires executive approval and extensive planning.

## Conducting a Successful DR Test

1. **Define the Scope and Objectives:** What exactly are you testing? (e.g., "Failover the ERP system to the AWS secondary region and verify database integrity within 2 hours.")
2. **Develop a Test Plan:** Create a detailed script of actions, timelines, and responsible individuals.
3. **Establish Success Criteria:** How do you know the test was successful? (e.g., Application responds to queries, RTO < 4 hours, RPO < 15 minutes).
4. **Execute and Monitor:** Run the test script. Document timestamps for every action taken. Note any deviations, errors, or unexpected behaviors.
5. **Post-Test Review (After Action Report):**
    * What went well?
    * What failed or was delayed?
    * What documentation needs to be updated?
    * Establish a remediation plan for identified issues.
6. **Update the DRP:** Incorporate lessons learned into the official Disaster Recovery Plan.
