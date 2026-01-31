# soc-alert-investigations
Sanitized SOC alert investigation write-ups from hands-on blue team training.
# Malware Alert Investigation

## Alert Overview
- **Alert Type:** Malware Detection
- **Severity:** Medium
- **Source:** Endpoint / Network Monitoring
- **Environment:** Simulated SOC Lab

## Initial Indicators
- Suspicious file or process activity detected
- Abnormal network behavior observed
- Alert triggered by security monitoring controls

## Logs and Data Analyzed
- Endpoint activity logs
- Network traffic logs
- Related authentication or system events

## Investigation Steps
1. Reviewed alert details and associated indicators.
2. Analyzed relevant logs to validate suspicious behavior.
3. Correlated network activity with endpoint events.
4. Assessed whether activity aligned with known malicious patterns.

## Findings
- Indicators were consistent with malicious behavior.
- Activity could not be attributed to legitimate system processes or user behavior.

## Conclusion
- **Alert Classification:** True Positive
- **Impact:** Potential compromise of endpoint system.

## Recommended Actions
- Isolate affected system.
- Remove malicious files or processes.
- Reset potentially compromised credentials.
- Monitor for further suspicious activity.

## Notes
This investigation was conducted as part of hands-on SOC analyst training using simulated alerts and environments.
