# DevSecOps-Pro
Notes for future / Exam

> install ansible program
```bash
pip3 install ansible==6.2.0
```

> create inventory file
```bash
cat > inventory.ini <<EOL

[devsecops]
devsecops-box-eggkd08x

[sandbox]
sandbox-eggkd08x

[prod]
prod-eggkd08x

EOL
```
> To see which hosts in our inventory matches a supplied group name, let’s try the following command.
```bash
ansible -i inventory.ini prod --list-hosts
```

> find available modules
```bash
ansible-doc -l
```
