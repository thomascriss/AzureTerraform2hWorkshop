2-hour Azure Terraform Workshop

Goals:

Using Terraform infrastructure-as-code, create a Virtual Network and Virtual Machine in Azure.

Prerequisites:

Azure Subscription with contributer access or higher
Azure CLI 2.8 or higher
Terraform 0.12 or higher

Copy or download and extract the source files from this repository.


Update variables.tf
1. Update subscription_id to your Azure subscription ID, which can be found by navigating to subscriptions in the Azure portal or by using the Azure CLI command $ az account list
2. Update location to your preferred location, e.g. East US 2. A full list can be found here: https://azure.microsoft.com/en-us/global-infrastructure/locations/

Run Terraform

1. Log in using the Azure CLI. Open a command prompt and type $ az login
2. Change your working directory to the location of the main.tf file
3. Run $ terraform init. This will initialize terraform in the current working directory. It is safe to run this command multiple times.
4. Run $ terraform plan. This creates an execution plan, and can be saved to a file using -out. This command without -out is informational and not necessary to deploy changes.
5. Run $ terraform apply. This applies the changes between the terraform files and the statefile. This command may sometimes need to be ran multiple times to reach the desired state of the configuration.

Verify changes
1. Navigate to the Azure portal and sign in
2. Click on your name in the top-right and ensure you are working in the desired directory
2. Navigate to Resource Groups and find the group specified in the Terraform plan or apply output.
3. Verify all resources have been created.
    
