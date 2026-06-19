# Project 8 – Linux File Integrity Investigation

## Objective

This project demonstrates how a SOC Analyst can monitor file integrity using SHA-256 hashing. By creating a baseline hash, modifying the file, and verifying it again, unauthorized changes can be detected quickly.

---

## Skills Demonstrated

- SHA-256 checksum generation
- Baseline hash creation
- File integrity verification
- Detecting unauthorized file modifications
- Linux file metadata analysis
- File permission inspection

---

## Tools Used

- Kali Linux
- sha256sum
- stat
- ls

---

## Steps Performed

### 1. Created the investigation file

Created `important.txt` containing sample data for integrity monitoring.

**Screenshot:** `01-file-created.png`

---

### 2. Generated the original SHA-256 hash

Calculated the initial checksum of the file.

```bash
sha256sum important.txt
```

**Screenshot:** `02-original-sha256-hash.png`

---

### 3. Saved the baseline hash

Stored the checksum in `baseline_hash.txt` for future verification.

```bash
sha256sum important.txt > baseline_hash.txt
cat baseline_hash.txt
```

**Screenshot:** `03-baseline-hash-saved.png`

---

### 4. Modified the file

Simulated unauthorized modification by changing the file contents.

```bash
echo "Unauthorized modification detected." > important.txt
cat important.txt
```

**Screenshot:** `04-file-modified.png`

---

### 5. Calculated the new SHA-256 hash

Generated a new checksum after modification.

```bash
sha256sum important.txt
```

The new hash differed from the baseline, indicating the file contents had changed.

**Screenshot:** `05-modified-sha256-hash.png`

---

### 6. Verified integrity against the baseline

Compared the current file with the stored baseline hash.

```bash
sha256sum -c baseline_hash.txt
```

Result:

```
important.txt: FAILED
WARNING: 1 computed checksum did NOT match
```

This confirms that the file integrity was compromised.

**Screenshot:** `06-hash-verification-failed.png`

---

### 7. Examined file metadata

Viewed timestamps, ownership, inode, and permissions.

```bash
stat important.txt
```

**Screenshot:** `07-file-stat-details.png`

---

### 8. Checked file permissions

Reviewed file permission settings.

```bash
ls -l important.txt
```

**Screenshot:** `08-file-permissions.png`

---

## Investigation Summary

| Check | Result |
|---------|--------|
| Baseline hash created | ✅ Yes |
| File modified | ✅ Yes |
| Hash changed | ✅ Yes |
| Integrity verification failed | ✅ Yes |
| Metadata reviewed | ✅ Yes |
| Permissions inspected | ✅ Yes |

---

## SOC Analyst Takeaway

File integrity monitoring is an essential defensive security practice. By maintaining baseline cryptographic hashes and periodically verifying them, security teams can quickly identify unauthorized modifications, potential malware activity, or evidence tampering during incident response.