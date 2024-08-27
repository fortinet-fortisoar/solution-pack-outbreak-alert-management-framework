| [Home](../README.md) |
| -------------------- |

# Using Pluggable Threat Hunting Framework

The Pluggable Threat Hunting framework is designed to integrate various threat detection tools, such as FortiSIEM, FortiAnalyzer, QRadar, and Splunk, for efficient outbreak alert threat hunting. The framework supports the following hunting categories:

- **Fabric Hunting**
- **Indicator of Compromise (IOC) Hunting**
- **Signature Hunting**

## Configuring and Using Pluggable Threat Hunting

1. **Saving Action Playbooks**

   All action playbooks related to Threat Detection Integration must be saved in the `05-Hunt` playbook collection. This collection serves as a repository for all the hunting playbooks, ensuring that they are organized and easily accessible.

>[!NOTE]
> The *`05-Hunt`* playbook collection is a part of SOAR Framework solution pack.

2. **Tagging Threat Hunting Playbooks**

   Each threat hunt playbook must be tagged with a specific identifier to facilitate its retrieval and execution. The tagging convention follows the format `[ThreatDetectionIntegration_Hunting]`. For example:

   - **Fortinet Fabric Hunt Playbooks**:
     - `Fortinet_FortiAnalyzer_Fabric_Hunting`
     - `Fortinet_FortiSIEM_Fabric_Hunting`
     
   - **IOC Hunt Playbooks**:
     - `Fortinet_FortiAnalyzer_IOC_Hunting`
     - `Fortinet_FortiSIEM_IOC_Hunting`
     - `IBM_QRadar_IOC_Hunting`
     - `Splunk_IOC_Hunting`
     
   - **Signature Hunt Playbooks**:
     - `Fortinet_FortiAnalyzer_Signature_Hunting`
     - `Fortinet_FortiSIEM_Signature_Hunting`
     - `IBM_QRadar_Signature_Hunting`
     - `Splunk_Signature_Hunting`

3. **Configuring the Outbreak Response Framework**

   The **Outbreak Response Framework Configuration Wizard** widget retrieves all selected threat detection integration playbook IRIs (Internal Resource Identifiers) that have been tagged with `[ThreatDetectionIntegration_Hunting]`. The widget then stores these IRIs in the key store module's record named `outbreak-threat-hunting-workflow-config`.

4. **Executing Threat Hunting Operations**

   When the Outbreak Response Framework performs Fabric, IOC, or Signature hunting for a specific outbreak alert, it fetches the relevant playbook's IRI from the `outbreak-threat-hunting-workflow-config` record. The framework then calls the associated hunting playbook to execute the threat hunt operation.

This integration and execution strategy ensures that SOC analysts can efficiently hunt for threats using their preferred detection tools, streamlining the response to outbreak alerts.

# Next Steps

| [Installation](./setup.md#installation) | [Configuration](./setup.md#configuration) | [Usage](./usage.md) |
|-----------------------------------------|-------------------------------------------|---------------------|