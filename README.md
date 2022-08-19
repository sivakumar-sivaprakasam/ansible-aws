# ansible-aws

Steps to provision EC2 instance for Ansible:

- Instance Type: Amazon Linux or Ubuntu
- Instance Class: t2.micro
- Userdata script:
```
#!/bin/bash
sudo apt update
sudo apt install -y
sudo apt install python3-boto3 python3-botocore python3-boto -y
```

Once the instance is provisioned, login to the instance & check if Ansible is correctly installed

```
ansible --version
```

Please don't forget to create IAM Role with "AdministratorAccess" policy and attach it to newly created instance