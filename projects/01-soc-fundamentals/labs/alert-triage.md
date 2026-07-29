# SOC Alert #001 - Multiple Failed SSH Login Attempts

## Alert Information

| Field | Value |
|---|---|
| Alert ID | SOC-001 |
| Detection Source | SIEM |
| Category | Authentication Attack |
| Severity | Medium |
| Status | Under Investigation |

---

# Scenario

The SIEM generated an alert after detecting multiple failed SSH login attempts against a Linux server.

The activity originated from an external IP address attempting to authenticate with different usernames.

The SOC analyst must investigate the alert and determine if the activity represents a real security incident.

---

# Initial Alert Details

## Observed Activity

- Protocol: SSH
- Target Asset: Linux Server
- Event Type: Failed Authentication
- Source: External IP Address
- Number of Attempts: 50 failed login attempts
- Time Window: 10 minutes

---

# Investigation Steps

## 1. Validate the Alert

The analyst checks:

- Number of failed attempts
- Source IP reputation
- Target system importance
- Usernames targeted
- Authentication logs

---

## 2. Log Analysis

Example log:
Failed password for invalid user admin from 185.xxx.xxx.xxx port 22 ssh2
Failed password for root from 185.xxx.xxx.xxx port 22 ssh2
Failed password for test from 185.xxx.xxx.xxx port 22 ssh2

---

# Analysis

The activity indicates a possible SSH brute force attack.

Indicators:

- Multiple authentication failures
- Targeting privileged accounts
- External source address
- Automated username guessing

---

# MITRE ATT&CK Mapping

Technique:

**T1110 - Brute Force**

Tactic:

**Credential Access**

---

# Severity Assessment

## Impact

Potential unauthorized access to the Linux server.

## Likelihood

High because the attacker is actively attempting credential guessing.

## Final Severity

Medium / High

---

# SOC Response Actions

Recommended actions:

1. Block malicious IP address
2. Review successful SSH logins
3. Disable compromised accounts
4. Enforce MFA
5. Update detection rules

---

# Final Decision

Classification:

**True Positive - Brute Force Attempt**

The alert represents malicious activity requiring security response.

---

# Lessons Learned

- Monitor authentication failures
- Implement account lockout policies
- Restrict SSH exposure
- Use strong authentication mechanisms