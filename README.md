# Ansible Sample Playbook for Oracle19c GI & DB requirements

## Procedure
### Ansible Installation (Centos8-stream)

```:Installing Python3.9
dnf -y module install python39
```

```:Installing sshpass
dnf -y install sshpass
```

```:Installing Ansible by PIP
pip3 install ansible
ansible --version
```

### Execution
1. Linux 1st step configurations
```:
cd projecto_debgon
ansible-playbook -i hosts 01_db_1st.yml
```

- SELinux configuration
- Timezone configuration
- Hostname configuration
- /etc/hosts configuration
- Network configurations (ex.IP Addresses)
- DNS Client configurations
- DNF Repositories configuration
- Package installations
- Service configurations
- Partition configurations
- LVM2 - VG configurations
- LVM2 - LV configurations
- Filesystem configurations


2. Then reboot the system
```:
ansible-playbook -i hosts 02_db_reboot.yml
```

3. Linux 2nd step configurations
```:
cd projecto_debgon
ansible-playbook -i hosts 03_db_2nd.yml
```

- Group configurations
- User configurations
- Directory configuration for Mount Points
- /etc/fstab configuration
- Directory configurations
- Kernel Parameter configurations
- User Limit configuration
- Udev Rule configurations

4. Then reboot the system
```:
ansible-playbook -i hosts 02_db_reboot.yml
```



