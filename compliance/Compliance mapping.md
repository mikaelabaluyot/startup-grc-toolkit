|Risk ID|Risk|Rating|Control|GDPR|NIST CSF 2.0|
|-|-|-|-|-|-|
|R1|Password reuse leads to third-party breaches, allowing attackers to authenticate to systems that holds sensitive data, causing unauthorised disclosure.||Multi-Factor Authentication (MFA), enforced on all user accounts.|Article 32(1)(b),<br />32(2); <br />Article 5(1)(f)|PR.AA-03,<br />|
|R2|Phishing emails tricks administrators into disclosing credentials, compromising privileged accounts and access or alter sensitive data.||Security awareness training with phishing simulations. Phishing-resistant MFA for admin.<br />Separating least-privilege admin accounts. Email filtering.|Article 32(1)(b),<br />32(2),32(4).<br />Article 5(1)(f)|PR.AT-02,<br />PR.AA-03,<br />PR.AA-05|
|R3|Known and unpatched vulnerabilities are exploited by attackers, allowing unauthorised access to systems containing sensitive data.||Vulnerability management:<br />inventory of asset, regularly scanning of authentication.<br />Patch by severity.|Article 32(1)(b),32(1)(d),32(2):<br />Article 5(1)(f)|ID.RA-01, ID.RA-06,<br />PR.PS-02|
| R4|Insecure database configuration such as public exposure or default credentials, allowing unauthorized access to sensitive data held in the database.||Documented security baselines.<br />Scheduled configuration reviews and drift detection. |Article 32(1)(b),32(1)(d),32(2);<br />Article 25(2);<br />Article 5(1)(f)|PR.PS-01, DE.CM-09,<br />PR.AA-05|
|R5|Non document processes, ownership or evidence for GDPR obligations results in non-compliance(such as unlawful processing, missed breached notifications, unfulfilled data subject requests) will lead to regulatory fines and reputational damages. ||Privacy governance process:<br />named owners/DPO, records of processing as of Article 30, data subject request and breach procedures.|Article 5(2), 24(1),24(2),<br />30,83|GV.OC-03,GV.RR-O2,GV.PO-01,GV.OV-02|
|||||||



