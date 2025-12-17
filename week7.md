# Week 7: Security Audit and System Evaluation

## Overview
In Week 7 I completed a comprehensive security audit and system evaluation of the Ubuntu Server. All actions were performed remotely via SSH from the workstation. The audit checked system configuration, network exposure, access control enforcement, running services, SSH security, and any remaining risks.

---

## Lynis Security Scan
I ran a full Lynis security audit to identify configuration weaknesses and potential vulnerabilities. The scan output and remediation suggestions are shown here as a reference in Markdown format: `![Lynis Scan Results](assets/lynis_scan.png)`. Lynis provides a prioritized list of findings which I used to guide subsequent checks.

---

## Network Security Assessment
A network scan was performed from the workstation using nmap to validate open ports and firewall effectiveness. The scan results are referenced as: `![Nmap Scan](assets/nmap_scan.png)`. This confirms which services are network-exposed and helps verify the UFW policy.

---

## Access Control Verification
AppArmor (mandatory access control) was reviewed to ensure critical services are confined. Status and active profiles can be seen via: `![Access Control Status](assets/access_control.png)`. Enforced profiles reduce the impact of compromised processes.

---

## Running Services Audit
All currently active services were listed and reviewed to confirm only necessary services are running. Output is shown using: `![Running Services](assets/running_services.png)`. Any non-essential services were noted for removal or disabling to minimise the attack surface.

---

## SSH Security Verification
SSH access was tested to ensure only key-based authentication is allowed and password authentication is disabled. Evidence of successful key-based login is referenced as: `![SSH Verification](assets/ssh_verification.png)`.

---

## System Configuration Review
Critical configuration files and firewall rules were inspected to confirm previous hardening steps (SSH hardening, UFW rules, user privileges) are correctly applied. Example of configuration review: `![Config Review](assets/config_review.png)`.

---

## Remaining Risks
Residual issues that could not be fully mitigated during the audit were documented. A summary of remaining risks and recommended actions is provided here: `![Remaining Risks](assets/remaining_risks.png)`.

---

## Summary
The Week 7 audit confirms that the server is hardened, monitored, and constrained by AppArmor and firewall rules. The Markdown references for screenshots above (`![Lynis Scan Results](assets/lynis_scan.png)`, `![Nmap Scan](assets/nmap_scan.png)`, etc.) provide a clear record of evidence for the server’s security posture and remaining risks.
