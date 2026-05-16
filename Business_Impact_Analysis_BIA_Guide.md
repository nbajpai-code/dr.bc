# Business Impact Analysis (BIA) Guide

A Business Impact Analysis (BIA) is the foundational step in developing a robust Business Continuity Plan (BCP) and Disaster Recovery Plan (DRP). It identifies critical business functions, the resources required to support them, and the potential impact of a disruption.

## 1. Objectives of a BIA
* **Identify Critical Processes:** Determine which business functions are essential for survival.
* **Assess Financial and Operational Impacts:** Evaluate the cost of downtime over time.
* **Define Recovery Objectives:** Establish the Recovery Time Objective (RTO) and Recovery Point Objective (RPO) for each function.
* **Identify Dependencies:** Map dependencies on internal systems, third-party vendors, personnel, and physical facilities.

## 2. The BIA Process

### Phase 1: Information Gathering
1. **Identify Business Units:** List all major departments (e.g., HR, Finance, IT, Operations, Sales).
2. **Develop BIA Questionnaire:** Create a survey to gather data from department heads.
3. **Conduct Interviews:** Hold meetings with stakeholders to clarify responses and delve deeper into critical processes.

### Phase 2: Analysis and Assessment
1. **Impact Assessment:** Evaluate the impact of a disruption across different time intervals (e.g., 1 hour, 24 hours, 3 days, 1 week). Consider:
   * Financial Impact (lost revenue, penalties, fines).
   * Operational Impact (inability to deliver services).
   * Reputational Impact (loss of customer trust, brand damage).
   * Legal/Regulatory Impact (breach of contracts, compliance failures).
2. **Determine RTO and RPO:**
   * **RTO (Recovery Time Objective):** Maximum acceptable downtime.
   * **RPO (Recovery Point Objective):** Maximum acceptable data loss (in terms of time).
3. **Identify Resource Requirements:** What is needed to recover the process?
   * IT Systems and Applications.
   * Personnel (roles and numbers).
   * Physical Facilities and Equipment.
   * Third-party Services and Vendors.

### Phase 3: Reporting and Approval
1. **Draft BIA Report:** Summarize findings, prioritize business functions (e.g., Tier 1: Mission Critical, Tier 2: Important, Tier 3: Deferrable).
2. **Management Review:** Present the findings to executive leadership for approval. The approved BIA dictates the budget and scope for the DRP.

---

## 3. BIA Questionnaire Template

*Use this template to interview department heads or process owners.*

**Process Name:** ________________________
**Department:** __________________________
**Process Owner:** _______________________

**1. Process Description:**
*Briefly describe the business process and its primary purpose.*

**2. Impact of Disruption:**
*Rate the impact (None, Low, Medium, High, Critical) over the following timeframes:*
* **< 4 Hours:** Financial [ ], Operational [ ], Reputational [ ], Legal [ ]
* **24 Hours:** Financial [ ], Operational [ ], Reputational [ ], Legal [ ]
* **3 Days:** Financial [ ], Operational [ ], Reputational [ ], Legal [ ]
* **1 Week:** Financial [ ], Operational [ ], Reputational [ ], Legal [ ]

**3. Maximum Tolerable Downtime (MTD) / RTO:**
*What is the absolute maximum time this process can be down before the business suffers catastrophic consequences?* __________

**4. Maximum Tolerable Data Loss (RPO):**
*How much data loss can this process tolerate (e.g., 1 hour's worth, 24 hours' worth, zero data loss)?* __________

**5. IT Dependencies:**
*List the applications, databases, and network services required for this process.*

**6. Internal/External Dependencies:**
*List any other internal departments or external vendors required for this process.*

**7. Minimum Resource Requirements:**
*To operate in a degraded/recovery mode, what are the absolute minimum resources needed (staff, equipment, workspace)?*
