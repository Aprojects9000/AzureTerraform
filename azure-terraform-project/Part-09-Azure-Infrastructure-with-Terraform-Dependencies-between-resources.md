# Terraform - Azure - Part 9. Azure Infrastructure with Terraform - Dependencies between resources
In this project I am going to learn to use Terraform in Azure. The reason for learning Terraform over ARM templates (or Bicep) is that Terraform can be used on other cloud platforms such as AWS and Google Cloud. I am following along with the [Azure Infrastructure with Terraform](https://www.youtube.com/playlist?list=PLLc2nQDXYMHowSZ4Lkq2jnZ0gsJL3ArAw) playlist from Alan Rodrigues. Thanks Alan.

## Project Table of Contents

- [Part 1: Azure Infrastructure with Terraform - What and Why Terraform](Part-01-Azure-Infrastructure-With-Terraform-What-and-Why-Terraform.md)
- [Part 2: Azure Infrastructure with Terraform - Concepts when it comes to Terraform](Part-02-Azure-Infrastructure-with-Terraform-Concepts-when-it-comes-to-Terraform.md)
- [Part 3: Azure Infrastructure with Terraform - Terraform workflow](Part-03-Azure-Infrastructure-with-Terraform-Terraform-workflow.md)
- [Part 4: Azure Infrastructure with Terraform - Installing Terraform](Part-04-Azure-Infrastructure-with-Terraform-Installing-Terraform.md)
- [Part 5: Azure Infrastructure with Terraform - Creating a resource group](Part-05-Azure-Infrastructure-with-Terraform-Creating-a-resource-group.md)
- [Part 6: Azure Infrastructure with Terraform - Creating an Azure Storage Account](Part-06-Azure-Infrastructure-with-Terraform-Creating-an-Azure-Storage-Account.md)
- [Part 7: Azure Infrastructure with Terraform - Terraform state](Part-07-Azure-Infrastructure-with-Terraform-Terraform-state.md)
- [Part 8: Azure Infrastructure with Terraform - Creating a container and a blob](Part-08-Azure-Infrastructure-with-Terraform-Creating-a-container-and-a-blob.md)
- [Part 9: Azure Infrastructure with Terraform - Dependencies between resources](Part-09-Azure-Infrastructure-with-Terraform-Dependencies-between-resources.md)
- [Part 10: Azure Infrastructure with Terraform - Destroying the resources](Part-10-Azure-Infrastructure-with-Terraform-Destroying-the-resources.md)
- [Part 11: Azure Infrastructure with Terraform - Using Variables](Part-11-Azure-Infrastructure-with-Terraform-Using-Variables.md)
- [Part 12: Azure Infrastructure with Terraform - Lab - Creating an Azure virtual network](Part-12-Azure-Infrastructure-with-Terraform-Lab-Creating-an-Azure-virtual-network.md)
- [Part 13: Azure Infrastructure with Terraform - Lab - Creating an Azure virtual machine](Part-13-Azure-Infrastructure-with-Terraform-Lab-Creating-an-Azure-virtual-machine.md)
- [Part 14: Azure Infrastructure with Terraform - Quick note on accessing Azure resource properties](Part-14-Azure-Infrastructure-with-Terraform-Quick-note-on-accessing-Azure-resource-properties.md)
- [Part 15: Azure Infrastructure with Terraform - Lab - Create Public IP Address](Part-15-Azure-Infrastructure-with-Terraform-Lab-Create-Public-IP-Address.md)
- [Part 16: Azure Infrastructure with Terraform - Lab - Adding data disks](Part-16-Azure-Infrastructure-with-Terraform-Lab-Adding-data-disks.md)
- [Part 17: Azure Infrastructure with Terraform - Lab - Availability Sets](Part-17-Azure-Infrastructure-with-Terraform-Lab-Availability-Sets.md)
- [Part 18: Azure Infrastructure with Terraform - Lab- Custom Script extensions](Part-18-Azure-Infrastructure-with-Terraform-Lab-Custom-Script-extensions.md)

## Part 1 Table of Contents

- [Intro](#intro)
- [Result](#result)


# Project

<a id="intro"></a>

## Intro

In this part we'll talk about dependencies between resources. 


<a id="result"></a>

## Result

## [Part 9: Azure Infrastructure with Terraform - Dependencies between resources](https://www.youtube.com/watch?v=JLS_r9ugwJ0&list=PLLc2nQDXYMHowSZ4Lkq2jnZ0gsJL3ArAw&index=9) 

Resources have dependencies. To create a Blob for instance, you need a container. That Container in turn has the dependency of a Storage Account, and that Storage Account in turn needs a Resource Group. To make sure resources only get deployed when all dependencies are in place, you can add a "depends condition" to the respective resource block. 

The order of your configuration file does not determine the order in which Terraform will deploy the resources. 
    
    This can explain the error message I got when trying to deploy the configuration file in the last part. If the container and blob are being deployed before the storage account, there's nothing it refers to yet. Still doesn't explain why it does work with the internal Terraform naming system, but it might have to do with it. 

    It does have to do with it. I tried both with and without the dependency conditions. With the condition it deploys everything in one go, without it it fails to find the resource group for the storage account, or the storage account for the container and blob. I can see in the deployment process that it starts with trying to deploy the container, then resource group, then blob, then storage account. Only the resource group was created, which makes sense as it doesn't have any dependencies (that weren't previously created). Good to know.

    Interesting that if you use the Terraform naming system to refer to other resources it fixes the issue of deployment errors caused by dependencies.

Adding the depends condition will ensure all necessary dependencies are in place. 

The depends condition looks like so:
```
depends_on = [
    resource_type.resource_name
]
```
It is good practice to include any dependencies to your resource blocks. Having said that, let's add the dependency of each resource to it's resource block via the use of the depends condition. Here's an example of one resource block with the depends condition added:

```
resource "azurerm_storage_blob" "sample" {
  name                   = "sample.txt"
  storage_account_name   = "storageaccount7654345678"
  storage_container_name = "data"
  type                   = "Block"
  source                 = "sample.txt"
  depends_on = [
    azurerm_storage_container.data
]
}
```

That was it. As always, don't forget to delete your resources if you're done with studying for the moment.


Errors:
There was a 404 error when it tried to deploy the storage account. This was because I reffered to the resource group through a string, but apparently then you need to use the actual resource name. Not the resource block name as when using the Terraform reference system. 


## []() 


