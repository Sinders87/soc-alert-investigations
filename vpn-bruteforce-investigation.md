# VPN Brute Force Alert Investigation

## Alert Overview
- **Alert Type:** Possible Brute Force Attack
- **Severity:** High
- **Event ID:** 162
- **Event Time:** Jun 21, 2023, 01:51 PM
- **Detection Rule:** SOC210 – Possible Brute Force Detected on VPN
- **Analyst Level:** Security Analyst
- **Environment:** Simulated SOC Lab

## Host Information
- **Hostname:** Mane
- **Domain:** LetsDefend
- **Operating System:** Windows 10 (64-bit)
- **IP Address:** 172.16.17.210
- **Primary User:** Mane
- **System Role:** Client
- **Last Login:** Jun 21, 2023, 12:00 PM

## Initial Indicators
- Multiple failed VPN authentication attempts were observed for a valid user account.
- A successful VPN login occurred shortly after the failed attempts from the same source IP address.
- This sequence of activity triggered a brute force alert based on authentication behavior.

## Authentication and Network Details
- **Username:** mane@letsdefend.io
- **Source IP Address:** 37.19.221.229
- **Destination Address:** 33.33.33.33
- **Destination Hostname:** vpn-letsdefend.io
- **Login Outcome:** Successful login following repeated failures

## Logs and Data Analyzed
- VPN authentication logs showing failed and successful login attempts.
- Raw authentication event data indicating incorrect password attempts followed by success.
- Host login information associated with the affected user account.
- External IP reputation analysis for the source IP address.

## Investigation Steps
1. Reviewed the alert details to understand the sequence of failed and successful login attempts.
2. Analyzed VPN authentication logs to confirm multiple failed logins from a single external IP address.
3. Verified that a successful login occurred shortly after the failed attempts using the same source IP.
4. Identified the source IP as external to the organization.
5. Performed reputation analysis on the source IP using threat intelligence sources.
6. Assessed whether the login pattern was consistent with brute force behavior.
7. Evaluated the potential impact on the affected user account and system.

## Findings
- The source IP address was external and associated with suspicious activity.
- Multiple failed login attempts were followed by a successful authentication using the same user account.
- The login pattern strongly indicated a successful brute force attack against VPN credentials.
- IP reputation analysis showed the source IP had been flagged by security vendors as malicious.
- No immediate evidence of lateral movement or further malicious activity was observed after login.

## Conclusion
- **Alert Classification:** True Positive
- **Impact:** VPN account credentials were likely compromised through brute force techniques.
- **Status:** Brute force attack successfully identified through log correlation.

## Recommended Actions
- Reset the affected user’s credentials immediately.
- Enforce multi-factor authentication (MFA) on VPN access.
- Block or restrict the source IP address at the network perimeter.
- Review VPN authentication policies, including lockout thresholds.
- Monitor for additional suspicious authentication attempts across other accounts.

## Notes
This investigation was conducted as part of hands-on SOC analyst training using simulated alerts and environments. All information has been sanitized and does not contain proprietary or sensitive data.
