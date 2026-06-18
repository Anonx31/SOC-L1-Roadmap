# Incident Timeline

## Project 2 - Brute Force and Account Lockout Investigation

### Date: June 13-14, 2026

#### Failed Login Attempts (Event ID 4625)

* 11:50:01 PM - Failed Login Attempt
* 11:50:07 PM - Failed Login Attempt
* 11:50:10 PM - Failed Login Attempt
* 11:50:13 PM - Failed Login Attempt
* 11:50:17 PM - Failed Login Attempt
* 11:50:22 PM - Failed Login Attempt
* 11:51:02 PM - Failed Login Attempt
* 11:51:51 PM - Failed Login Attempt
* 11:53:18 PM - Failed Login Attempt

#### Account Lockout (Event ID 4740)

* 11:53:18 PM - Account Locked

#### Account Recovery

* Account manually unlocked by administrator

#### Successful Login (Event ID 4624)

* 12:06:48 AM (June 14, 2026) - Successful Login

---

## Investigation Summary

### Target Account

targetuser

### Failed Login Attempts

9

### Account Lockout

Yes

### Successful Login After Unlock

Yes

### Event IDs Investigated

* Event ID 4625 – Failed Login Attempt
* Event ID 4740 – Account Lockout
* Event ID 4624 – Successful Login

### Findings

A series of failed login attempts were observed against the account "targetuser". After multiple authentication failures, Windows automatically locked the account. Following administrative intervention and account recovery, a successful login was recorded.

### Security Assessment

The observed activity resembles a brute-force attack scenario where repeated incorrect password attempts triggered the account lockout policy. No evidence of unauthorized access was identified during the investigation.

### Recommendation

* Maintain account lockout policies.
* Monitor repeated failed login attempts.
* Investigate unusual authentication activity.
* Enforce strong password policies.
