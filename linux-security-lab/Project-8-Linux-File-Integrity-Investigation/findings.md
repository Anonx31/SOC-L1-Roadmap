# Key Findings

## Successful Actions

- Created a baseline SHA-256 checksum.
- Stored the checksum for later verification.
- Simulated unauthorized file modification.
- Verified file integrity against the baseline.
- Examined metadata and permissions.

## Security Observation

The integrity verification process detected that the file had been altered after the baseline was created.

## Impact

Any mismatch between the current hash and the baseline indicates that the file contents have changed and should be investigated further.

## Recommendation

- Maintain secure baseline hashes for critical files.
- Perform regular integrity checks.
- Investigate unexpected checksum mismatches immediately.
- Combine file integrity monitoring with centralized logging and alerting.