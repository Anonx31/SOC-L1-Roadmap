# Investigation Report

## Case Information

- **Project:** Linux Log Analysis & Authentication Investigation
- **Platform:** Kali Linux
- **Investigator:** Bobby Dsouza
- **Status:** Completed

---

## Investigation Summary

A review of Linux authentication and system logs was performed to identify unusual login behavior, unauthorized access attempts, or suspicious privilege escalation events.

The investigation included analysis of system journals, authentication sessions, login history, active users, kernel logs, and sudo activity.

---

## Evidence Collected

### 1. System Journal

Reviewed the latest journal entries using:

```bash
journalctl -n 50
```

Observed routine service operations and scheduled background tasks.

---

### 2. Session Logs

Reviewed authentication session events using:

```bash
journalctl | grep -i "session"
```

Multiple user sessions were successfully created and terminated as expected.

---

### 3. Login History

Examined historical logins using:

```bash
last
```

The system contained normal login records without suspicious patterns.

---

### 4. Active User Verification

Verified current logged-in users using:

```bash
who
```

One active user (`anon`) was identified.

---

### 5. User Identity

Reviewed account information using:

```bash
id
```

Confirmed user ID and group memberships associated with the active account.

---

### 6. Kernel Messages

Inspected recent kernel logs:

```bash
dmesg | tail -20
```

Messages primarily referenced VirtualBox guest integration and expected system components.

---

### 7. Sudo Activity

Reviewed privilege escalation events:

```bash
journalctl | grep sudo
```

Observed legitimate sudo sessions initiated by the user with successful session creation and closure.

---

### 8. Reboot History

Checked reboot records:

```bash
last reboot
```

No abnormal reboot activity was identified.

---

## Findings

| Category | Result |
|-----------|--------|
| Unauthorized Login Attempts | Not observed |
| Failed Authentication | Not identified |
| Suspicious User Sessions | None detected |
| Unexpected Sudo Usage | Not observed |
| Kernel Warnings | No critical security concerns |
| Active User | anon |

---

## Analyst Assessment

The collected evidence indicates normal system operation. Authentication events, session creation, and sudo activity appear consistent with legitimate administrative usage.

No indicators of compromise or unauthorized access were identified during this investigation.

---

## Final Verdict

**Status: No suspicious authentication or log activity detected.**

The examined logs reflect expected user behavior and routine system operations.