# Timeline

| Step | Activity |
|------|----------|
| 1 | Created `important.txt` for monitoring |
| 2 | Generated SHA-256 hash of the original file |
| 3 | Saved the baseline hash to `baseline_hash.txt` |
| 4 | Modified the contents of `important.txt` |
| 5 | Generated a new SHA-256 hash |
| 6 | Compared the file against the stored baseline |
| 7 | Verification failed because the hashes did not match |
| 8 | Reviewed file metadata using `stat` |
| 9 | Checked file permissions using `ls -l` |