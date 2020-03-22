# Laba9 Terraform create vm

TASK:
Create new Azure instance(VM) via terraform

---

**Step 1:** Install Azure CLI to Terraform Server
```sudo curl -sL https://aka.ms/InstallAzureCLIDeb | sudo bash```

**Step 2:** Create authentication using a Service Principal with a Client Secret
Firstly, login to the Azure CLI using: ```az login``` then type ```az ad sp create-for-rbac --name "terraform-server"``` [more](https://www.terraform.io/docs/providers/azurerm/guides/service_principal_client_secret.html)

**Step 3** Storing the credentials as Environment Variables.
```
#!/bin/bash

echo "--------------------------------------------------"

export ARM_CLIENT_ID="00000000-0000-0000-0000-000000000000"
export ARM_CLIENT_SECRET="00000000-0000-0000-0000-000000000000"
export ARM_SUBSCRIPTION_ID="00000000-0000-0000-0000-000000000000"
export ARM_TENANT_ID="00000000-0000-0000-0000-000000000000"

echo "--------------------------------------------------"
```
for testing connection:
```az login --service-principal -u $ARM_CLIENT_ID -p $ARM_CLIENT_SECRET --tenant $ARM_TENANT_ID```
```az login --service-principal --username 00000000-0000-0000-0000-000000000000 --password 00000000-0000-0000-0000-000000000000 --tenant 00000000-0000-0000-0000-000000000000```

**Step 3:** Need to run command ```terraform init```
