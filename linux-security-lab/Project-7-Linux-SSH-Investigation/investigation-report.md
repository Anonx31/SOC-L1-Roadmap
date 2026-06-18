# Linux SSH Investigation Report

## Summary

A security review of the SSH service and configuration was performed on a Kali Linux system.

## Observations

### SSH Service

- Service Name: ssh.service
- Status: Inactive (dead)
- Startup: Disabled

### Running Processes

The only SSH-related process observed was:

- ssh-agent

No active `sshd` daemon process was running.

### Network Exposure

Port 22 was checked using:

```bash
ss -tulpn | grep :22
```

Result:

- No listening service detected.
- System is not accepting inbound SSH connections.

### Authentication Configuration

Observed settings:

- PermitRootLogin: commented (default)
- PasswordAuthentication: enabled

### Login History

Historical user sessions were visible using `last`.

No suspicious login patterns were identified.

### Current Sessions

The `who` command showed only one active local session:

- anon

### Journal Logs

System logs mainly contained ssh-agent initialization events and no evidence of remote authentication attempts.

## Security Assessment

| Item | Status |
|-------|--------|
| SSH Server Installed | Yes |
| SSH Running | No |
| Port 22 Listening | No |
| Remote Access Active | No |
| Suspicious Activity Found | No |

## Conclusion

The investigation found no indicators of compromise or unauthorized SSH access. The system is not currently exposing SSH services over the network.