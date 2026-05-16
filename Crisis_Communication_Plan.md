# Crisis Communication Plan

Technical recovery is only half of Disaster Recovery. Effective communication is essential to maintain trust with customers, employees, and stakeholders during a crisis.

## Principles of Crisis Communication
1. **Transparency:** Be honest about what you know and what you don't know. Do not speculate.
2. **Timeliness:** Communicate early and frequently. Silence breeds panic and rumor.
3. **Accuracy:** Ensure all facts are verified before release.
4. **Empathy:** Acknowledge the impact the disruption is having on users and stakeholders.

## Communication Channels
Establish primary and alternative channels, assuming normal systems (like corporate email or Slack) might be down.
* **Internal:** Emergency mass notification systems (e.g., Everbridge, PagerDuty), SMS blasts, out-of-band communication platforms (e.g., a secondary Slack workspace, WhatsApp groups).
* **External:** Public status page (hosted on external infrastructure, e.g., Atlassian Statuspage), social media (Twitter/X, LinkedIn), dedicated support hotlines.

## Key Audiences

### 1. Internal Employees
* **Message:** Safety instructions (if physical disaster), current status of the business, instructions on work location (e.g., work from home), and updates on system availability.
* **Cadence:** Hourly initially, then daily.

### 2. The Disaster Recovery Team / IT Staff
* **Message:** Technical updates, bridge call information, assigned tasks.
* **Cadence:** Continuous via dedicated incident management channels.

### 3. Customers / Users
* **Message:** Acknowledgment of the issue, what services are impacted, what the company is doing to resolve it, and estimated time to resolution (if known).
* **Cadence:** Initial message within 15 minutes of verified incident. Updates every 30-60 minutes depending on severity.

### 4. Executive Stakeholders & Board of Directors
* **Message:** High-level summary of the incident, impact on revenue/brand, timeline for recovery, and resource requests.
* **Cadence:** Dictated by the Incident Commander; usually at major milestones.

### 5. Media / Public Relations
* **Message:** Carefully crafted statements coordinated by PR and Legal.
* **Cadence:** As needed. *Technical staff should never speak directly to the media without authorization.*

## Templates

### Template: Initial Outage Notification (External - Status Page)
**Subject/Headline:** Investigating: Service Disruption Affecting [Service Name]
**Body:** We are currently investigating an issue affecting [Service/Feature]. Users may experience [describe impact, e.g., inability to log in, degraded performance]. Our engineering teams are engaged and working to identify the root cause. We will provide an update within [XX] minutes. We apologize for the inconvenience.

### Template: Update Notification (External - Status Page)
**Subject/Headline:** Update: Service Disruption Affecting [Service Name]
**Body:** We have identified the issue causing the disruption to [Service Name]. The root cause appears to be [brief, non-technical explanation if safe to share, otherwise omit]. Our teams are actively implementing a fix. We anticipate restoration of service by [Time/Date, only if highly confident]. Next update in [XX] minutes.

### Template: Resolution Notification (External - Status Page)
**Subject/Headline:** Resolved: Service Disruption Affecting [Service Name]
**Body:** The issue affecting [Service Name] has been fully resolved. Services are operating normally. We apologize for any disruption this caused to your operations. A full post-incident review (RCA) will be conducted, and we will share relevant findings to prevent future occurrences.
