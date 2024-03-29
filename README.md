# Release Information 

- **Version**: 1.1.0![](./docs/res/icon-preview.svg)
- **Certified**: Yes
- **Publisher**: Fortinet
- **Compatible Version**: 7.4.0 and later
- [**Release Notes**](./release_notes.md)
  
<table>
    <tr>
        <th>NOTE</th>
        <td>Preview releases are a beta release. This means that release is intended to get feedback and might not be best suited for production level deployments. The functionality might change in backward-incompatible ways or have limited support. A beta release is not subject to any SLA, Quality Assurance or deprecation policy. Feature availability and support for preview releases will continue to improve as the solution/feature matures.</td>
    </tr>
</table>

# Overview 
Outbreak Response Framework provides vital information about ongoing cybersecurity attacks that affect numerous companies, organizations, and industries. The goal is to notify organizations about the latest cybersecurity threats and empower them to take proactive measures to secure their systems. 
 
## Outbreak Alerts
A new FortiGuard Outbreak Detection Service is now available through FortiSOAR&trade;'s **Outbreak Response Framework** Solution Pack.

FortiGuard Alerts typically provide details about emerging threats and security incidents. These alerts include information such as the type of threat (e.g., malware, ransomware, phishing), the targeted systems or applications, the potential impact, and recommended actions to mitigate the risk.

You might find specifics about the characteristics of the threat, such as its propagation methods, known vulnerabilities it exploits, and any indicators of compromise (IoCs) that can help identify its presence in a network. Additionally, FortiGuard Outbreak Alerts may offer insights into the threat actor or group behind the attack and their motives.

The **Outbreak Response Framework** solution pack investigates the Outbreak Alert that contains the following information:

- A narrative of the attack containing the following, its timeline, and affected technologies:

    - **Description**: Detailed information on the vulnerability

    - **Background**: Reasons and factors involved in vulnerability exposure

    - **Announcement**: Zero-day information on the vulnerability

    - **Latest Developments**: Measures taken to prevent vulnerability

    - **CVE List**: CVEs that provide a reference for publicly known information-security vulnerabilities and exposures

- List of Indicators of Compromise(IOCs)

## Outbreak Dashboard

The **Outbreak Response Overview** dashboard gives the Outbreak information in easy to understand visuals:

![Outbreak Dashboard](./docs/res/dashboard-outbreak-response-overview.png)
 
## Threat Hunt Rules
The **Outbreak Response Framework** solution pack investigates the Outbreak alert using its associated Threat Hunt Rules. Every Outbreak alert has the following three types of Threat Hunt Rules:

1. **Fortinet Fabric Rules**: Currently, the **Outbreak Response Framework** solution pack provides the following two types of Fortinet Fabric rules:

    1. **FortiAnalyzer**: FortiAnalyzer is a centralized logging and reporting appliance designed by Fortinet for their Fortinet Security Fabric. It plays a crucial role in handling outbreaks by collecting, analyzing, and reporting on security events and logs from various Fortinet security devices deployed throughout an organization. Here's how FortiAnalyzer typically manages outbreak alerts:

        1. Centralized Logging

        2. Real-time Monitoring

        3. Threat Detection and Analysis

        4. Log Correlation

        5. Alerting and Notification

        6. Historical Analysis

        7. Reporting and Visualization

    2. **FortiSIEM**: FortiSIEM is a Security Information and Event Management (SIEM) solution offered by Fortinet. It provides organizations with comprehensive security information and event management capabilities, enabling them to detect, respond to, and mitigate security threats. Here's how FortiSIEM typically handles outbreaks:

        1. Log Collection and Aggregation

        2. Real-time Monitoring

        3. Behavioral Analysis

        4. Threat Intelligence Integration

        5. Incident Detection and Response

        6. Forensic Analysis

        7. Incident Workflow and Collaboration

        8. Reporting and Compliance

2. **Sigma Rules (Signature-Based Threat Hunt Rules)**:  Sigma rules play a crucial role in threat detection and are especially valuable in the context of outbreak alerts. Sigma is a generic and open standard for writing cybersecurity detection rules that helps share and collaborate on threat detection strategies across different security platforms.

    Here's how Sigma rules help detect outbreak alerts:

    1. *Consistency Across Platforms*: Sigma rules are platform-agnostic, meaning they can be translated and implemented on various Security Information and Event Management (SIEM) systems. This consistency allows organizations to use the same rule set across different security tools, promoting a unified and streamlined approach to threat detection.

    2. *Rapid Rule Development*: Sigma provides a simple and expressive language for creating detection rules. This simplicity helps security teams rapidly develop and deploy the rules without going through the intricacies of each specific SIEM or security solution. In the context of outbreak alerts, this agility is crucial for quickly responding to emerging threats.

    3. *Community Collaboration*: Sigma rules can be shared and contributed to by the cybersecurity community. This collaborative approach enables security professionals to benefit from each other's expertise and quickly adapt to new threat landscapes. In the case of outbreak alerts, having a community-contributed rule can provide early detection capabilities for the latest threats.

    4. *Granular Threat Detection*: Sigma rules can be fine-tuned to detect specific behaviors or patterns associated with an outbreak. Whether identifying known indicators of compromise (IoCs) or recognizing unusual network traffic patterns, Sigma rules allow for granular and targeted threat detection, enhancing the ability to detect outbreaks early.

    5. *Adaptability to New Threats*: Outbreak alerts often involve new and evolving threats. You can modify and adapt Sigma rules to address the characteristics of emerging threats. This adaptability is crucial in staying ahead of cyber criminals who constantly enhance their tactics, techniques, and procedures (TTPs).

3. **YARA Rules**: YARA rules help detect outbreaks and other security threats. It is a pattern-matching and rule-based language designed to help researchers and defenders identify and classify malware based on textual or binary patterns. Here's how YARA rules can be beneficial in detecting outbreak alerts:

    1. *Pattern Matching*: YARA rules allow for the definition of specific patterns or signatures associated with malicious files or behaviors. In the context of outbreak alerts, these patterns could include unique strings, file structures, or other characteristics that indicate a particular malware or threat.

    2. *Flexibility and Customization*: YARA rules are highly flexible and can be customized to target specific threat attributes. Security researchers can create rule sets that focus on the unique features of an outbreak, allowing for precise detection tailored to the distinct characteristics of the threat.

    3. *Scalability*: YARA rules can be scaled to cover a range of files and activities. This scalability is crucial in case of outbreaks where the volume of malicious activity is significant. You can apply YARA rules to large datasets for identifying and isolating hostile entities.

    4. *Indicators of Compromise (IoCs)*: You can use YARA rules to define IoCs associated with an outbreak. These could include file hashes, registry entries, or network behavior patterns. By incorporating these IoCs into YARA rules, organizations can automate the detection of malicious entities based on known indicators.

    5. *Community Collaboration*: YARA rules benefit from community collaboration, similar to Sigma rules. Security professionals often share YARA rules to help others detect and respond to emerging threats. This collaborative approach enables a broader and more collective defense against outbreaks.

    6. *Integration with Security Systems*: YARA rules can be integrated into various security systems, including antivirus solutions and intrusion detection systems. This integration allows for real-time detection and response to outbreaks, enhancing the overall security posture of an organization.

    7. *Behavioral Analysis*: While based on static patterns, YARA rules can also incorporate behavioral aspects of malware. Hence, you can design YARA rules to detect known signatures and suspicious or malicious behavior, contributing to more dynamic threat detection.


# Next Steps
| [Installation](./docs/setup.md#installation) | [Configuration](./docs/setup.md#configuration) | [Usage](./docs/usage.md) | [Contents](./docs/contents.md) |
|----------------------------------------------|------------------------------------------------|--------------------------|--------------------------------|
