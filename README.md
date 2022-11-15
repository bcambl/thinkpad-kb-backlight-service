Thinkpad keyboard backlight service
===================================
Re-enable Thinkpad keyboard backlight after reboot/sleep/suspend/hibernate on linux.

Tested on Intel T490 & AMD P14s Gen2 running Fedora 36.

### Automated installer with ansible playbook

re-enable keyboard backlight upon wake from sleep or reboot with keyboard brightness set to low (1 x Fn+Space):
```
ansible-playbook --ask-become-pass -i localhost, install.yml -e ansible_connection=local
```

re-enable keyboard backlight upon wake from sleep or reboot with keyboard brightness set to high (2 x Fn+Space):
```
ansible-playbook --ask-become-pass -i localhost, install.yml -e ansible_connection=local -e brightness=2
```
