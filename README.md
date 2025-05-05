## ✅ Step-by-Step Terraform Installation on Ubuntu
#### 1. Update System
```bash
sudo apt update && sudo apt upgrade -y
```
#### 2. Install Required Packages
```bash
sudo apt install -y gnupg software-properties-common curl
```
#### 3. Add HashiCorp GPG Key
```bash
curl -fsSL https://apt.releases.hashicorp.com/gpg | sudo gpg --dearmor -o /usr/share/keyrings/hashicorp-archive-keyring.gpg
```
#### 4. Add HashiCorp APT Repository
```bash
echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] https://apt.releases.hashicorp.com $(lsb_release -cs) main" | \
sudo tee /etc/apt/sources.list.d/hashicorp.list
```
#### 5. Update and Install Terraform
```bash
sudo apt update
sudo apt install -y terraform
```
#### 6. Verify Installation
```bash
terraform -version
```
You should see something like:

Terraform v1.8.x