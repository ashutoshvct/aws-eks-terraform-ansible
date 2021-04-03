# aws-eks-terraform-ansible
Create AWS EKS cluster using terraform and ansible. And Deploy an App.

#### Launch Amazon linux 2 and add this part in user-data:

```bash
#!/bin/bash
yum update
yum install git -y
amazon-linux-extras install ansible2 -y
ansible-galaxy collection install community.general
git clone https://github.com/ashutoshvct/aws-eks-terraform-ansible.git
sleep 10s
cd aws-eks-terraform-ansible && nohup ansible-playbook install_eks.yaml -vv &
```
