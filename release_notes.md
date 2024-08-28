# What's New

#### Outbreak Management - A New Look!

Get ready to experience a revamped Outbreak Management interface designed to streamline your workflow and enhance your visibility. When you click *Outbreak Management* in the navigation menu, you’re greeted with an intuitive layout featuring these powerful tabs:

- **Dashboard**: Stay informed with a dynamic Outbreak Response Overview, showcasing:
    - Outbreak Status (Last 30 Days)
    - KEVs For Outbreak CVEs (Last 30 Days)
    - Recent Outbreaks Detected
    - Top 10 Outbreak Threat Feeds
    - …and so much more!

- **Outbreaks**: Access comprehensive records of all outbreak alerts at your fingertips.

- **Hunt Rules**: Explore and manage Fortinet Fabric Rules, Sigma Rules, and YARA Rules linked to your outbreak response solution packs.

#### Wizard Enhancements

The wizard has received several key upgrades, making your configuration process smoother and more efficient:

- Each integration now has its dedicated configuration tab for a more organized setup experience.
  
- Take control of your security operations by automating investigation frequencies and tailoring your investigation windows to fit your needs.
  
- Never miss an update! Opt for automatic installation and get near-instant notifications when outbreak-specific solution packs are available.

- A brand-new **Ingest Now** button on the *Summary* page allows you to install the latest outbreak response solution packs instantly.

#### New Widgets Added

We’ve added cutting-edge widgets to boost your productivity:

- **Playbook Execution Wizard**: Simplify and streamline your playbook execution with an intuitive, user-friendly wizard.

- **Playbook Buttons**: Execute your playbooks with a single click, directly from the dashboard.

- The picklist *Rule Type* has been renamed to **Threat Hunt Rule Type**.

- The picklist *Record Status* has been renamed to **Outbreak Alert Status** to provide clearer context and more specific terminology, reflecting its focus on outbreak-related alerts. This change enhances user understanding and aligns with the outbreak management system's terminology, making it easier for analysts to identify and manage relevant alerts.
    - This picklist has additional options - `New` and `Deactivate`.
    - The picklist item *Active* has been renamed to **Tracking**.

- The addition of the following Record Sets aims to enhance the configuration experience by offering more granular control and customization options:
    - `outbreak-threat-hunt-tools`
    - `outbreak-auto-install-time-frame`
    - `outbreak-threat-hunt-tools-params`

- The following hunt playbooks have been moved to SOAR Framework's **05 - Hunt** playbook collection to consolidate all hunt-related playbooks in one location. This reorganization simplifies navigation and management by keeping all hunt playbooks together, which streamlines processes and reduces confusion. As a result, the hunt playbooks in **10 - SP - Outbreak Response Framework** have been deprecated to prevent redundancy and to ensure that users can easily find and execute hunt playbooks within a single, cohesive framework:

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

- Removed Ticketing/ITSM integration page from the configuration wizard

- The dependency on the following connectors as IT/SM tools and their presence in the configuration wizard has been removed to simplify the setup process and streamline operations. By eliminating these connectors, the system reduces complexity, minimizes potential points of failure, and enhances performance. This change also reflects a shift towards a more integrated and automated environment, where essential functions are handled natively within the outbreak management framework, reducing reliance on external tools and ensuring a more seamless user experience:
    - Azure Log Analytics
    - Fortinet FortiGate
    - Jira
    - ServiceNow