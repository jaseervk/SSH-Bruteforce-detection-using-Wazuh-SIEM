## Wazuh Agent Configuration

```bash
nano /var/ossec/etc/ossec.conf
```
Add follwing rulues:
```bash
<localfile>
  <log_format>journald</log_format>
  <location>systemd</location>
</localfile>
```

## Restart Agent:
```bash
systemctl restart wazuh-agent
```
