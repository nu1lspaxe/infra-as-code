# infra-as-code

## Vagrant
```bash
# If you're in WSL2
vagrant plugin install virtualbox_WSL2
export VAGRANT_WSL_ENABLE_WINDOWS_ACCESS="1"
# And disable Hyper-V, install Oracle Virtual Box

# To install hashicorp/precise64 (virtual machine)
vagrant init hashicorp/precise64

# Start virtual machine
vagrant up

# Check exist machine types
vagrant box list

# Get SSH information
vagrant ssh-config
# Connect to vm in ssh
ssh -p <PORT> -i <PATH_TO_PRIVATE_KEY> vagrant@<SSH_IP>

# Reload virtual machine
vagrant reload
```

## Ansible
```bash
# Run yaml file
ansible-playbook <filename>

# default host config file: /etc/ansible/hosts
```

## Terraform

### vault_0x01

```bash
vault server -dev -dev-root-token-id root -dev-tls

# Set environment variables in new terminal
# export VAULT_ADDR='https://127.0.0.1:8200'
# export VAULT_CACERT='/tmp/vault-tls<random>/vault-ca.pem'
```

```bash
terraform init
terraform plan -out=plan.out   # generate terraform.tfstate
terraform apply --auto-approve plan.out
```
