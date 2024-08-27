| [Home](../README.md) |
|----------------------|

# Usage

In this section, we detail the various user flows to understand the scenarios where this solution pack’s automation may address your needs.

## Outbreak Response Framework Flowchart 
 
 <!-- ![Outbreak Alerts Flowchart](./res/outbreak-alert-flow.svg) -->

The following is an ideal flow to use the **Outbreak Response Framework** solution pack:

1. Install **Outbreak Response Framework** solution pack.

2. Complete the *Outbreak Response Framework*'s **Configuration Wizard**. The [Setup](./setup.md#setup-outbreak-response-framework-on-fortisoar) section details the configuration process.

3. Install individual *Outbreak Response* solution packs. You can specify if the outbreak response solution packs are installed automatically.

    Additionally, to install outbreak response solution packs, click **Ingest Now** button on the summary page.
    
>[!Note]
>The [**EXAMPLE: Outbreak Response - Progress MOVEit Transfer SQL Injection Vulnerability**](#example-outbreak-response---progress-moveit-transfer-sql-injection-vulnerability) section explains the response of **Outbreak Response Framework** solution pack to *Progress MOVEit Transfer SQL Injection Vulnerability* by way of an example.

4. **Fetch CVEs for KEVs**: Using NIST integration FortiSOAR checks if an associated CVE is tagged as a KEV. Once found, it creates CVE records in the vulnerability module and links those records to outbreak alerts.

5. **Ingest IOCs as Threat Feeds**: IOCs associated with the Outbreak are ingested as threat feeds in FortiSOAR using Fortinet FortiGuard Outbreak connector.

    Users are notified and the alert severity is raised if an alert containing these IOCs is found in FortiSOAR.

6. **IOC Threat Hunt**: You can perform IOC Threat Hunt, and create IOC hunt alerts of type *Outbreak* in FortiSOAR, using any of the following:

    - Fortinet Fabric solutions (FortiSIEM/FortiAnalyzer)

    - Other SIEM solutions (QRadar/Splunk)

7. **Sigma Rules**: You can perform signature Based Threat Hunt using Sigma Rules:

    1. Perform Signature-based Threat Hunting using Fortinet Fabric solutions (FortiSIEM/FortiAnalyzer) and create alerts of type *Outbreak* in FortiSOAR.

        ![FortiSIEM Fabric Rule](./res/fsm_fortinet_fabric.png)

        ![FortiAnalyzer Fabric Rule](./res/faz_fortinet_fabric.png)

    2. Perform Signature-based Threat Hunting using other SIEM solutions (QRadar/Splunk/Azure Log Analytics) and create alerts  of type *Outbreak* in FortiSOAR.

        ![Signature Based Threat Hunting Rules](./res/sigma_rule.png)

8. **Remediation**: We can take remediation using two ways

    1. **Automatically**: FortiSOAR automatically blocks indicators, of type **_IP_** and **_URL_**, using the FortiGate Integration. For rest of the indicators, a FortiSOAR task is created.

    2. **Manually**: FortiSOAR automatically creates a FortiSOAR task to block all the indicators using the FortiGate Integration.

9. **Mitigation**: For every Outbreak Alert have associated mitigation. FortiSOAR provides the mitigation recommendations using public sources, like patch available, etc.

    ![Mitigation](./res/mitigation.png)

## Example: Outbreak Response - Progress MOVEit Transfer SQL Injection Vulnerability

Before performing the steps outlined in this section, we recommend setting the global variable `Demo_mode` to `true`. Once done, the following steps generate example data for a better understanding of this solution packs functionality.

1. Install **Outbreak Response Framework** Solution Pack.

2. Complete the *Outbreak Response Framework*'s **Configuration Wizard**.

3. Activate the **Create Ticket in ITSM Tools** playbook, under the **10 - SP - Outbreak Response Framework** playbook collection, to create tickets to track and manage hunts. Perform this step only if you have added a ticketing/ITSM solution in the configuration wizard.

4. Install **Outbreak Response - Progress MOVEit Transfer SQL Injection Vulnerability**.

5. Navigate to the **Outbreak Management** menu and select **Outbreak Alerts** to view the following screen:

    ![](./res/outbreak-alerts-moveit.png)

6. Click to open the alert and view the following screen that contains description and background information:

    ![](./res/outbreak-alerts-moveit-details.png)

7. Click the **Execute** button and select **Investigate Outbreak** to begin investigation. Since the global variable `Demo_mode` is set to `true`, you are given example data to view and understand the information retrieved from investigation.

    ![](./res/outbreak-alerts-moveit-investigate-outbreak.png)

8. Scroll the alert details page to view CVE IDs, correlations, and alerts, apart from other information:

    ![](./res/outbreak-alerts-moveit-more-details.png)

    The following information becomes available as the **Outbreak Response** solution pack creates the following:

    1. Outbreak Alerts: The outbreak alerts contain the following

        - Outbreak Alert details

        - Mitigation Details

    2. Threat Hunt Rules: The following rules are created with the solution pack:

        - Yara Rules: YARA Rules help malware researchers identify and classify malware samples that focus on scanning and identifying malicious files.

        ![Yara Rules](./res/yara_rule.png)

        - Sigma Rules: Sigma Rules provide a standard format for log events. They are helpful in searching or pattern matching through log data.
        
        Using Sigma Rules we can create signature-based Threat Hunt Rules for various Threat Detection Integrations like SIEM, Analyzer, or EDR.
        
        - Fortinet Fabric Rules: With every Outbreak Alert FortiGuard provides FortiAnalyzer and FortiSIEM as part of Fortinet fabric solution.

9. Head over to the **Dashboard** and select **Outbreak Response Overview** to view following information.

    ![Outbreak Dashboard](./res/dashboard-outbreak-response-overview.png)

<!-- ## Workaround - Uniqueness Constraint Violation

Under demo mode when *Threat Hunting - FortiAnalyzer - Get Related Assets* playbook creates an asset, a uniqueness constraint violation occurs. This section offers a workaround.

1. Navigate to **Automation** > **Playbooks**.

2. Click to open the **10 - SP - Outbreak Response Framework** playbook collection.

3. Click to open the **Threat Hunting - FortiAnalyzer - Get Related Assets** playbook.

4. Double-click to open **Create Asset** step.

5. Click the Correlations tab under **Fields**.

6. Select **Overwrite** and then **Append**.

7. Click **Save** and **Save Playbook** to save the changes to the playbook. -->

# Next Steps

| [Installation](./setup.md#installation) | [Configuration](./setup.md#configuration) | [Contents](./contents.md) |
|-----------------------------------------|-------------------------------------------|---------------------------|