# Release Information 

 * **Version**: 1.0.0 
 * **Certified**: Yes 
 * **Publisher**: Fortinet 
 * **Compatible Version**: 7.2.0 and later 
 

 # Overview 
 Outbreak Response Framework provides key information about on-going cybersecurity attack with significant ramifications affecting numerous companies, organizations and industries. The goal is to keep organizations informed about the latest cybersecurity threats and empower them to take proactive measures to secure their systems. 
 
 ## Outbreak Alerts
 A new FortiGuard Outbreak Detection Service is now available through the FortiSOAR Solution Pack "Outbreak Response Framework". 
 
 FortiGuard Alerts typically provide details about emerging threats and security incidents. These alerts include information such as the type of threat (e.g., malware, ransomware, phishing), the targeted systems or applications, the potential impact, and recommended actions to mitigate the risk.
 
 You might find specifics about the characteristics of the threat, such as its propagation methods, known vulnerabilities it exploits, and any indicators of compromise (IoCs) that can help identify its presence in a network. Additionally, FortiGuard Outbreak Alerts may offer insights into the threat actor or group behind the attack and their motives.
 
 "Outbreak Response Framework" investigate the Outbreak Alert which contains the following information
 - A narrative of the attack, its timeline and affected technologies.
    - Description: It contains the detail information of the vulnerability
    - Background: It contains the how this vulnerability is expose 
    - Announcement: It contains the zero day information of the vulnerability
    - Latest Developments: It contains the what kind of measures are taken to prevent vulnerability
    - CVE List: It contains which CVE's that provides a reference method for publicly known information-security vulnerabilities and exposures
 - - List of Indicators of Compromise(IOCs).
 
 ## Threat Hunt Rules
 "Outbreak Response Framework" solution pack investigate the Outbreak Alert automatically using its associated Threat Hunt Rules. Every Outbreak Alert have following three types of Threat Hunt Rules.

 - Fortinet Fabrics Rules: Currently "Outbreak Response Framework" solution pack provides below two types of Fortinet Fabrics rules
    1. FortiAnalyzer: FortiAnalyzer is a centralized logging and reporting appliance designed by Fortinet for their Fortinet Security Fabric. It plays a crucial role in handling outbreaks by collecting, analyzing, and reporting on security events and logs from various Fortinet security devices deployed throughout an organization. Here's how FortiAnalyzer typically handles outbreaks:
        a.Centralized Logging
        b. Real-time Monitoring
        c. Threat Detection and Analysis
        d. Log Correlation
        e. Alerting and Notification
        f. Historical Analysis
        g. Reporting and Visualization

    2. FortiSIEM: FortiSIEM is a Security Information and Event Management (SIEM) solution offered by Fortinet. It is designed to provide organizations with comprehensive security information and event management capabilities, enabling them to detect, respond to, and mitigate security threats. Here's how FortiSIEM typically handles outbreaks:
        a. Log Collection and Aggregation
        b. Real-time Monitoring
        c. Behavioral Analysis
        d. Threat Intelligence Integration
        e. Incident Detection and Response
        f. Forensic Analysis
        g. Incident Workflow and Collaboration
        h. Reporting and Compliance

 - Sigma Rules (Signature Based Threat Hunt Rules):  Sigma rules play a crucial role in threat detection and are especially valuable in the context of outbreak alerts. Sigma is a generic and open standard for writing cybersecurity detection rules in a consistent and standardized way, making it easier to share and collaborate on threat detection strategies across different security platforms.
 Here's how Sigma rules can be useful in detecting outbreak alerts:
    1. Consistency Across Platforms: Sigma rules are designed to be platform-agnostic, meaning they can be translated and implemented on various security information and event management (SIEM) systems. This consistency allows organizations to use the same set of rules across different security tools, promoting a unified and streamlined approach to threat detection.
    2. Rapid Rule Development: Sigma provides a simple and expressive language for creating detection rules. This allows security teams to rapidly develop and deploy rules without needing to learn the intricacies of each specific SIEM or security solution. In the context of outbreak alerts, this agility is crucial for quickly responding to emerging threats.
    3.Community Collaboration: Sigma rules can be shared and contributed to by the cybersecurity community. This collaborative approach enables security professionals to benefit from each other's expertise and quickly adapt to new threat landscapes. In the case of outbreak alerts, having a community-contributed rule can provide early detection capabilities for the latest threats.
    4. Granular Threat Detection: Sigma rules can be finely tuned to detect specific behaviors or patterns associated with an outbreak. Whether it's identifying known indicators of compromise (IoCs) or recognizing unusual network traffic patterns, Sigma rules allow for granular and targeted threat detection, enhancing the ability to catch outbreaks early.
    5. Adaptability to New Threats: Outbreak alerts often involve new and evolving threats. Sigma rules can be easily modified and adapted to address the characteristics of emerging threats. This adaptability is crucial in staying ahead of cybercriminals who constantly modify their tactics, techniques, and procedures (TTPs).

- Yara Rules: Yara rules are another powerful tool in the realm of cybersecurity, and they are particularly useful for detecting outbreaks and other security threats. Yara is a pattern-matching and rule-based language designed to help researchers and defenders identify and classify malware based on textual or binary patterns. Here's how Yara rules can be beneficial in detecting outbreak alerts:
    1. Pattern Matching: Yara rules allow for the definition of specific patterns or signatures associated with malicious files or behaviors. In the context of outbreak alerts, these patterns could include unique strings, file structures, or other characteristics that are indicative of a particular malware or threat.
    2. Flexibility and Customization: Yara rules are highly flexible and can be customized to target specific attributes of a threat. Security researchers can create rules that focus on the unique features of an outbreak, allowing for precise detection tailored to the specific characteristics of the threat.
    3. Scalability: Yara rules can be scaled to cover a wide range of files and activities. This scalability is crucial in the context of outbreaks where the volume of malicious activity may be significant. Yara rules can be efficiently applied to large datasets to identify and isolate malicious entities.
    4. Indicators of Compromise (IoCs): Yara rules can be used to define IoCs associated with an outbreak. These could include file hashes, registry entries, or network behavior patterns. By incorporating these IoCs into Yara rules, organizations can automate the detection of malicious entities based on known indicators.
    5. Community Collaboration: Similar to Sigma rules, Yara rules benefit from community collaboration. Security professionals often share Yara rules to help others detect and respond to emerging threats. This collaborative approach enables a broader and more collective defense against outbreaks.
    6.Integration with Security Systems: Yara rules can be integrated into various security systems, including antivirus solutions and intrusion detection systems. This integration allows for real-time detection and response to outbreaks, enhancing the overall security posture of an organization.
    7. Behavioral Analysis: While Yara rules can be based on static patterns, they can also incorporate behavioral aspects of malware. This means that Yara rules can be designed to detect not only known signatures but also suspicious or malicious behavior, contributing to more dynamic threat detection.




Note: This is a beta playbook, which lets you implement and test pre-release software. Since the playbook is beta, it might contain bugs. Updates to the pack during the beta phase might include non-backward compatible features. We appreciate your feedback on the quality and usability of the pack to help us identify issues, fix them, and continually improve.


 # Next Steps
 | [Installation](./docs/setup.md#installation) | [Configuration](./docs/setup.md#configuration) | [Usage](./docs/usage.md) | [Contents](./docs/contents.md) | 
 |--------------------------------------------|----------------------------------------------|------------------------|------------------------------|