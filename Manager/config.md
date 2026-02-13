### SSH Brute Force Custom Rule

```bash
nano /var/ossec/etc/rules/local_rules.xml
```

Add follwing rules:
```bash
<group name="ssh_bruteforce,">

  <!-- Fast brute force: 8 failed logins in 60 seconds from same IP -->
  <rule id="100500" level="12">
    <if_matched_sid>5710</if_matched_sid>
    <frequency>8</frequency>
    <timeframe>60</timeframe>
    <same_source_ip />
    <description>SSH brute force detected - 8 failures in 60 seconds from same IP</description>
    <mitre>
      <id>T1110</id>
      <tactic>Credential Access</tactic>
    </mitre>
  </rule>

</group>
```

## Restart manager:
```bash
systemctl restart wazuh-manager
```
