| [Home](../README.md) |
|----------------------|

# Upgrade Instructions

This section points out some actions to take after the upgrade to **Outbreak Response Framework** `v2.0.0`.

> **IMPORTANT**: Follow these instructions closely and do not skip.

## Prerequisites

- Upgrade Fortinet FortiAnalyzer connector to `v3.3.0` or later

<!-- ## Before upgrade

 1. 
 
 2. 
 
 3.  -->

## After Upgrade

Perform these actions after a successful upgrade to **Outbreak Response Framework** `v2.0.0`.

1. Edit the picklist **Outbreak Alert Status**. For information on editing picklists, refer (Editing Picklist)[https://docs.fortinet.com/document/fortisoar/7.6.0/administration-guide/97786/application-editor#Picklist_Editor] on FortiSOAR product documentation.

2. Add a new picklist item **Deactivated**

3. Open the playbook **> Investigate Outbreak Alert** under the playbook collection *10 - SP - Outbreak Response Framework*.

4. Edit the playbook step **Update Last Pull Time**.

5. Scroll down to the **Status** field and set it to **`Tracking`**.

3. Open the playbook **Outbreak Alert Time Frame Analysis** under the playbook collection *10 - SP - Outbreak Response Framework*.

4. Edit the playbook step **Update Outbreak Alert Status**.

5. Scroll down to the **Status** field and set it to **`Deactivated`**.

6. Run the **Outbreak Response Framework** configuration wizard again. Refer to the section [Configuration Wizard](./setup.md#setup-outbreak-response-framework-on-fortisoar).

