| [Home](../README.md) |
| -------------------- |

# Contents

The **Outbreak Response Framework** solution pack contains the following resources.

## Picklist

| Name                                                    | Description                                                                                                 |
|:--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| AlertType![Removed](./res/icon-removed.svg)             | List of Alert Type (Added "Outbreak Alert" item)                                                            |
| Outbreak Alert Severity                                 | List of outbreak severity item values (Medium, High and Critical)                                           |
| Threat Hunt Rule Type![Renamed](./res/icon-renamed.svg) | (Previously *Rule Type*) List of Outbreak Alert Threat Hunt Rule item values (Yara, Sigma, Fortinet Fabric) |
| Threat Hunt Tools                                       | List of Threat Hunt Integration item value which will used for Threat Hunting                               |
| Outbreak Alert Status![Renamed](./res/icon-renamed.svg) | (Previously *Record Status*) List of Outbreak Alert status item value(Active, Resolved)                     |

## Record Sets

| Name                                | Description                                                                                                                              |
|:------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| `outbreak-threat-hunt-tools`        | Saves the names of outbreak hunt tools and helps the outbreak configuration wizard to select the required tools.   |
| `outbreak-auto-install-time-frame`  | Saves the number of days for which the outbreak response solution packs are set to install during configuration.   |
| `outbreak-threat-hunt-tools-params` | Saves the outbreak hunt tools parameters and helps the outbreak configuration wizard to populate these parameters. |

## Module Schema

| Name              | Description                                                       |
|:------------------|:------------------------------------------------------------------|
| Threat Hunt Rules | A module that list the Yara, Sigma and Fortinet Fabric Hunt Rules |
| Outbreak Alerts   | A module that list the outbreak details                           |

## Connector

| Name                                 | Description                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|:-------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Azure Log Analytics                  | Log Analytics is a tool in the Azure portal that's used to edit and run log queries against data in the Azure Monitor Logs store. This connector facilitates the automated operations related to query and saved searches.                                                                                                                                                                                                                               |
| Fortinet FortiAnalyzer               | FortiAnalyzer is the NOC-SOC security analysis tool built with operations perspective. With action-oriented views and deep drill-down capabilities, FortiAnalyzer not only gives organizations critical insight into threats, but also accurately scopes risk across the attack surface, pinpointing where immediate response is required.                                                                                                               |
| Fortinet FortiSIEM                   | FortiSIEM provides integrations that allow you to query and make changes to the CMDB, query events, and send incident notifications. Provide actions like get incidents, comment incident, cleared incident, get device details, get monitored organizations, report related actions and get all associated events for an incident from FortiSIEM.                                                                                                       |
| IBM QRadar                           | IBM QRadar is an enterprise security information and event management (SIEM) product. Fortinet FortiSOSR connector for IBM QRadar allows user to invoke QRadar API, perform Ariel Queries and operations like Get Offense,related events,update and close offenses.                                                                                                                                                                                      |
| Fortinet FortiGate                   | Fortinet FortiGate enterprise firewall provide high performance, consolidated advanced security and granular visibility for broad protection across the entire digital attack surface.                                                                                                                                                                                                                                                                   |
| Jira                                 | Jira Service Desk Connector for issue creating, updating and deleting.                                                                                                                                                                                                                                                                                                                                                                                   |
| NIST National Vulnerability Database | The NIST National Vulnerability Database (NVD) is the U.S. government repository of standards based vulnerability management data represented using the Security Content Automation Protocol (SCAP). This data enables automation of vulnerability management, security measurement, and compliance. The NVD includes databases of security checklist references, security related software flaws, misconfigurations, product names, and impact metrics. |
| ServiceNow                           | ServiceNow connector provides functionality to create, read, update and delete records of Table and Catalog type                                                                                                                                                                                                                                                                                                                                         |
| Splunk                               | Splunk connector allows users to invoke search, fetch events to related search, invoke alert actions, update notables, sync splunk users to FortiSOAR etc.                                                                                                                                                                                                                                                                                               |
| Fortinet FortiGuard Outbreak         | Fortinet FortiGuard Outbreak connector receives communication with *FortiGuard Outbreak Alerts* regarding an outbreak and its details. These alerts help understand the technical details of the attack and how organizations can protect themselves from the attack and others like it.                                                                                                                                                       |

## Widgets

| Name                                                | Description                                                                                                                                                                                                                   |
|:----------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Outbreak Response Framework Configuration Wizard    | Outbreak Response Framework Configuration Wizard has options to select the Threat Detection Integrations sources to run outbreak response hunt activities as part of your response or threat management strategy in FortiSOAR |
| Playbook Execution Wizard![new](./res/icon-new.svg) | The Playbook Execution Wizard widget renders playbook execution logs and related comments on the wizard                                                                                                                       |
| Playbook Buttons![new](./res/icon-new.svg)          | The Playbook Buttons widget creates playbook buttons on a records detailed view                                                                                                                                               |

## Roles

| Name                 | Description                                                                                                        |
|:---------------------|:-------------------------------------------------------------------------------------------------------------------|
| Full App Permissions | Essentially the root user, use carefully                                                                           |
| SOC Manager          | Responsible for Incident Investigation and other remediation and containment-related tasks.                        |
| SOC Analyst          | Responsible for Alert Triages, false-positive filtering, and escalating potentially malicious alerts to Incidents. |

## Playbook Collection

| 10 - SP - Outbreak Response Framework |
|:-------------------------------------:|

| Playbook Name                                               | Description                                                                                                                                  |
|:------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| Investigate Outbreaks (Type All)                            | Investigate New and Tracking outbreaks across various SIEM tools, then take action to remediate and mitigate them.                           |
| Investigate Outbreak                                        | Investigate the Outbreak Alert using various threat-hunting tools to understand the scope and impact of the threat                           |
| Stop Outbreak Alert Record Tracking                         | Update the status of the outbreak alert to "Resolved," and include the resolved notes and resolved reason in the associated outbreak alert.  |
| Find and Link Affected Assets                               | Examine vulnerabilities associated with the outbreak CVEs, and if any are found, identify the affected assets and link them to the outbreak. |
| Remediate and Mitigate Outbreak Response Alert              | Block all types of outbreak response alert indicators on the firewall according to their block status and take steps to mitigate them.       |
| Outbreak Alert Time Frame Analysis                          | Identify and deactivate outbreak alerts whose investigation time frame has expired.                                                          |
| Automated Deployment: Outbreak Alert Response Solution Pack | Automate Installation of Recent Outbreak Alert Solutions Pack (Last x Days) with Email Notification                                          |
| > Automated Deployment > Get Outbreak CVEs and IOC Details  | Retrieve Outbreak CVEs and IOC details, and set the last investigation time for newly installed outbreak alerts.                             |
| Configure Outbreak Response Framework                       | Set up the outbreak response framework, configure global value key store entries, and set up schedules for use in outbreak investigations.   |
| Get Outbreak CVEs and IOCs Details                          | Obtain outbreak alert CVE details from NIST and IOC information from Fortinet FortiGuard.                                                    |
| Find Known Exploited Vulnerabilities (KEV) CVEs             | Fetch Known Exploited Vulnerabilities (KEV) CVEs from NIST and create CVE record.                                                            |
| Find Known Exploited Vulnerabilities (KEV) CVEs             | Retrieve Known Exploited Vulnerabilities (KEV) CVEs from NIST and create a CVE record.                                                       |
| Create IOCs as Threat Intel Feeds                           | Obtain the IOCs from Fortinet FortiGuard and create the threat feeds in the Threat Intel module for the specified outbreak alert.            |

>[!Warning]
>We recommend that you clone these playbooks before customizing to avoid loss of information while upgrading the solution pack.

<!-- ![](./res/icon-known-issue.svg): Under demo mode when *Threat Hunting - FortiAnalyzer - Get Related Assets* playbook creates an asset, a uniqueness constraint violation occurs. For a possible solution, refer to the section **Usage** > **Workaround uniqueness constraint violation** [here](./usage.md#workaround---uniqueness-constraint-violation). -->

## System View

| Name                | Description                               |
|:--------------------|-------------------------------------------|
| Outbreak Management | Displays details of the selected outbreak |


# Next Steps

| [Installation](./setup.md#installation) | [Configuration](./setup.md#configuration) | [Usage](./usage.md) |
|-----------------------------------------|-------------------------------------------|---------------------|
