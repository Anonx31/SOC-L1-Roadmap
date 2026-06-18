# Investigation Timeline

| Step | Activity | Status |
|------|----------|--------|
| 1 | Reviewed latest system journal entries (`journalctl -n 50`) | ✅ Completed |
| 2 | Examined authentication session logs | ✅ Completed |
| 3 | Reviewed login history using `last` | ✅ Completed |
| 4 | Verified currently logged-in users with `who` | ✅ Completed |
| 5 | Confirmed account details using `id` | ✅ Completed |
| 6 | Reviewed recent kernel messages | ✅ Completed |
| 7 | Investigated sudo activity | ✅ Completed |
| 8 | Checked reboot history | ✅ Completed |
| 9 | Correlated findings across collected logs | ✅ Completed |
| 10 | Documented investigation results | ✅ Completed |

---

## Investigation Outcome

- No suspicious login attempts identified.
- Authentication sessions appeared legitimate.
- Sudo events reflected expected administrative activity.
- Kernel logs contained routine VirtualBox-related messages.
- Overall system behavior appeared normal.

**Final Status:** ✅ Investigation completed successfully with no indicators of compromise detected.