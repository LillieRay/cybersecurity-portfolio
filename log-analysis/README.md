# Log Analysis Lab

This section will include hands-on practice with log analysis using tools like:

- Splunk
- Wireshark
- Windows Event Viewer
- Azure Sentinel

# Coming Soon:
- Sample logs
- Notes from lab exercises
- Screenshots and alerts breakdowns
- What I learned

- ---

## Splunk Log Analysis Walkthrough

**Objective:** Investigate a potential brute-force attack using Splunk.

**Tools Used:**
- Splunk
- Sample authentication logs

**Steps:**
1. Loaded sample logs into Splunk.
2. Ran a search query to filter for failed login attempts:
3. index=auth sourcetype=linux_secure action=failure
4. 3. Identified a high number of failed logins from the same IP address.
4. Extracted IP, username, and timestamps for reporting.

**Outcome:**  
Discovered a brute-force attack attempt targeting the root user from IP `192.168.1.150`. Recommended blocking the IP and enforcing account lockout policy.
