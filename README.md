# k8s-from-scratch
Kubernetes from scratch using:  containerd_version: "2.0.0" , runc_version: "1.2.1" ,  cni_version: "v1.6.0" ,  kube_version: "1.31"



# Start the SSH service
```sudo systemctl enable ssh
sudo systemctl start ssh
```
# Generate SSH Key Pair 
ssh-keygen -t rsa -b 2048

# Copy SSH Public Key to Target Node
ssh-copy-id user@target-node-ip

# To run the playbook
ansible-playbook -i hosts.ini k8s-from-scratch.yml --ask-become-pass
