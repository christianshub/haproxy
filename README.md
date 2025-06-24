# HA Proxy setup

## VM provision through Terraform

```bash
cd terraform-provision-haproxy
terraform init -upgrade
terraform apply -parallelism=1 -lock=false
```

## HA Proxy config

```bash
cd ansible-config-haproxy
ansible-playbook -i inventory.ini playbooks/haproxy.yaml
```

## ⚠️ Important Notes

* After the VMs has been created its often possible to make the IP static through your routers network settings 