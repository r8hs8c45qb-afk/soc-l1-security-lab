# UC-01 — SSH Intrusion Detection & Response

## Summary
A simulated SSH intrusion attempt was detected from an unauthorized host in the lab environment.

## Environment
- Attacker: Kali Linux
- Target: Ubuntu Server
- Detection: Syslog + IDS alerts
- Role: SOC Level 1 Analyst

## Timeline
- T0 — SSH brute-force attempt detected
- T1 — Suspicious authentication failures logged
- T2 — Successful unauthorized access identified
- T3 — Incident validated and documented

## Detection Evidence
See evidence:
- evidence/screenshots/UC-01_ssh_detection_syslog.png
- evidence/screenshots/UC-01_ssh_intrusion_success.png

## Analyst Actions
- Reviewed authentication logs
- Correlated alerts from syslog and IDS
- Confirmed unauthorized access
- Documented incident and recommended mitigation

## Mitigation Recommendations
- Enforce SSH key authentication
- Disable password-based login
- Limit SSH access via firewall rules
- Monitor authentication logs continuously

## Conclusion
This incident demonstrates SOC Level 1 capabilities in detection, triage, and initial response to unauthorized access attempts.
