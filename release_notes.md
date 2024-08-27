# What's New

- **Outbreak Management** - A new look!
    Clicking the Outbreak Management in the navigation menu opens a page containing following tabs:
        - **Dashboard**: Displays the Outbreak Response Overview with visuals like:
            - Outbreak Status (Last 30 Days)
            - KEVs For Outbreak CVEs (Last 30 Days)
            - Recent Outbreaks Detected
            - Top 10 Outbreak Threat Feeds
            - and many more!
        - **Outbreaks**: Displays the outbreak alert records
        - **Hunt Rules**: Contains Fortinet Fabric Rules, Sigma Rules, and YARA Rules rules related to installed outbreak response solution packs

- Following new pages have been added:
    - **Configure Integration**: Contains separate configuration tab for each integration selected on the *Select Integration* page.
    - **Investigation Schedule**: Automate the investigation frequency and customize the investigation window.
    - **Installation & Notification**: Receive notifications when an outbreak specific solution pack becomes available and automatically install them.
    - Added a new **Ingest Now** button appears on the **Summary** page to install the latest outbreak response solution packs.

- The following widgets have been added to this solution pack:
    - Playbook Execution Wizard
    - Playbook Buttons

- The picklist *Rule Type* has been renamed to **Threat Hunt Rule Type**.
- The picklist *Record Status* has been renamed to **Outbreak Alert Status**.
    - This picklist has additional options - `New` and `Deactivate`.
    - The picklist item *Active* has been renamed to **Tracking**.

- Following *Record Sets* have been added:
    - `outbreak-threat-hunt-tools`
    - `outbreak-auto-install-time-frame`
    - `outbreak-threat-hunt-tools-params`

- The following hunt playbooks have been moved to SOAR Framework's *05 - Hunt* collection and hence *deprecated* in **10 - SP - Outbreak Response Framework**:

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

- Removed Ticketing/ITSM integration page

- Removed dependency on the following connectors as IT/SM tools are no longer supported:
    - Azure Log Analytics
    - Fortinet FortiGate
    - Jira
    - ServiceNow