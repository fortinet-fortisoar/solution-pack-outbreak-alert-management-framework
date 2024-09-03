## What's New

>[!NOTE]
>This solution pack requires FortiSOAR `v7.6.0` and later.

### Outbreak Management - A New Look!

Get ready to experience a revamped Outbreak Management, designed to streamline your investigation workflow and enhance your visibility of your environment to respond and remediate these Outbreak Alerts effectively and efficiently.

When you click Outbreak Management in the navigation menu, you’re greeted with an intuitive layout featuring these powerful tabs:

- **Dashboard**: Stay informed with a dynamic Outbreak Response Overview, showcasing:
    - Outbreak Status (Last 30 Days)
    - KEVs For Outbreak CVEs (Last 30 Days)
    - Recent Outbreaks Detected
    - Top 10 Outbreak Threat Feeds
    - …and so much more!

- **Outbreaks**: Access comprehensive records of all outbreak alerts at your fingertips.

- **Hunt Rules**: Explore and manage Fortinet Fabric Rules, Sigma Rules, and YARA Rules linked to your outbreak-specific response solution packs.

#### Improved Solution Pack Configuration Experience

The wizard has received several key upgrades, making your configuration process seamless:

- Each integration now has its dedicated configuration tab for a more organized setup experience and ensures that key configuration details are present.
  
- Take control of your security operations by automating investigation frequencies and tailoring your investigation windows to fit your needs.
  
- Never miss an update! Opt for automatic installation and get notified when outbreak-specific response solution packs are installed.

- A brand-new **Ingest Now** button on the *Summary* page allows you to install the latest outbreak-specific response solution packs instantly.

#### Improved Investigation Flow

- Introducing enhanced automation with the following new schedules to streamline outbreak response tasks:

    - `Investigate_Outbreak-Alerts`: Automatically identify new and ongoing outbreak alerts and forward them for thorough investigation using advanced threat-hunting tools.
    - `Outbreak_Alert-Time-Frame-Analysis`: Efficiently identify and deactivate outdated outbreak alerts based on their investigation time frame.
    - `Outbreak_Automated-Deployment-Outbreak-Alert-Response-Solution-Pack`: Seamlessly install the latest outbreak alert solutions pack (from the past X days) with automated email notifications.
    - `Outbreak_Ingest-Tracking-Outbreak-CVEs-and-IOCs`: Retrieve outbreak alert CVEs (KVE) from NIST and IOCs from Fortinet FortiGuard, focusing on those marked as ‘Tracking’.

- As an investigation result, we now create incidents in place of alerts.

#### Pluggable Threat Hunt Framework

The Pluggable Threat Hunting framework integrates threat detection tools, such as FortiSIEM, FortiAnalyzer, QRadar, and Splunk, for efficient outbreak alert threat hunting and integrates the following hunting categories:

- Fabric Hunting
- Indicator of Compromise (IoC) Hunting
- Signature Hunting

#### Widget Additions

We’ve integrated cutting-edge widgets to execute your playbooks with a single click and track the execution with an intuitive, user-friendly wizard.

- Playbook Execution Wizard
- Playbook Buttons

#### Picklist Enhancements

The following picklists and the containing items were renamed to provide clearer context and more specific terminology, reflecting its focus on outbreak-related alerts. This change enhances user understanding and aligns with the outbreak management system's terminology, making it easier for analysts to identify and manage relevant outbreak alerts.

- The picklist *Rule Type* has been renamed to **Threat Hunt Rule Type**.

- The picklist *Record Status* has been renamed to **Outbreak Alert Status**
    - This picklist has additional options - `New` and `Deactivate` to clearly indicate outbreak alerts' statuses.
    - The picklist item *Active* has been renamed to **Tracking** to mark that an outbreak alert is ready to investigate.

#### New Key Store Records

- The addition of the following Record Sets for use by the Configuration Wizard imparts a modular structure to threat hunt integrations and automatic installation of outbreak-specific response solution packs:
    - `outbreak-threat-hunt-tools`
    - `outbreak-threat-hunt-tools-params`
    - `outbreak-auto-install-time-frame`

- Effortlessly manage your threat hunt integrations. Each integration and its precise hunt parameters are stored in the `outbreak-threat-hunting-workflow-config` key store record, ensuring a streamlined and efficient threat-hunting process.

- Enjoy seamless automation with the installation of outbreak-specific response solution packs. All associated parameters are stored in the `outbreak-alert-config` key store record, providing an easy setup for optimal protection.

>[!NOTE]
> The `outbreak-threat-hunting-workflow-config` and the `outbreak-alert-config` key store records are created *after* the Outbreak Response Framework configuration completes.

#### Playbook Enhancements

- The following hunt playbooks are created within SOAR Framework's **05 - Hunt** playbook collection to consolidate all hunt-related playbooks in one location. This reorganization simplifies navigation and management by keeping all hunt playbooks together, which streamlines processes and reduces confusion:

    - IOC Hunting
    - IOC Hunting – FortiSIEM
    - IOC Hunting - FortiSIEM > Fetch Incident Associated Events
    - IOC Hunting - FortiAnalyzer
    - IOC Hunting - FortiAnalyzer > Device Log Search
    - IOC Hunting - Splunk
    - IOC Hunting - IBM QRadar
    - Threat Hunting (Fortinet Fabric) - FortiSIEM
    - Threat Hunting (Fortinet Fabric) - FortiSIEM > Fetch Incident
    - Threat Hunting (Fortinet Fabric) - FortiSIEM > Create Incident
    - Threat Hunting (Fortinet Fabric) - FortiSIEM > Fetch Associated Incident Events
    - Threat Hunting (Fortinet Fabric) - FortiAnalyzer
    - Threat Hunting (Fortinet Fabric) - FortiAnalyzer > Get Related Event Assets
    - Threat Hunting (Signature Based) - Splunk
    - Threat Hunting (Signature Based) - Splunk > Create Inbound Incident
    - Threat Hunting (Signature Based) - Splunk > Update Notable Fields
    - Threat Hunting (Signature Based) - IBM QRadar
    - Threat Hunting (Signature Based) - Get Events - FortiSIEM
    - Threat Hunting (Signature Based) - Get Events - FortiAnalyzer
    - Threat Hunting (Signature Based)  - FortiAnalyzer > Log Search

#### Miscellaneous Updates

We have streamlined our integrations by removing the following connectors from the Outbreak Response Framework:

- *Fortinet FortiGate*: Playbooks are now natively available in the SOAR Framework solution pack.
- *Azure Log Analytics*: Usage data indicates minimal engagement.
- *Jira* and *ServiceNow*: Integration no longer contributes to investigative processes.

The Ticketing/ITSM integration page has been removed from the Configuration Wizard.