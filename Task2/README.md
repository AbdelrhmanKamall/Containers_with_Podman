



EC2 hosts the Nginx container that is acting as the prox, so SSH in the public ec2 
```
mkdir -p ~/reverse-proxy
cd ~/reverse-proxy
vim nginx.conf
```
and this will have the nginx.conf



### 1. Create Required Secrets

```bash
echo "root" | podman secret create db_root_password -
echo "user" | podman secret create db_user -
echo "pass" | podman secret create db_password -
```