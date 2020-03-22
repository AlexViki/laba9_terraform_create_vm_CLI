# Laba9 Terraform create vm

TASK:
Create new Azure instance(VM) via terraform

---

**Step 1:** Install Azure CLI to Terraform Server
```sudo curl -sL https://aka.ms/InstallAzureCLIDeb | sudo bash```

**Step 2:** Create authentication using a Service Principal with a Client Secret
```az ad sp create-for-rbac --name "terraform-server"```
