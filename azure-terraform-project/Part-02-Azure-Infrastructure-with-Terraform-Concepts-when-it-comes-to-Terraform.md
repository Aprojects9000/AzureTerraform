# Terraform - Azure - Part 2: Azure Infrastructure with Terraform - Concepts when it comes to Terraform
In this project I am going to learn to use Terraform in Azure. The reason for learning Terraform over ARM templates (or Bicep) is that Terraform can be used on other cloud platforms such as AWS and Google Cloud. I am following along with the [Azure Infrastructure with Terraform](https://www.youtube.com/playlist?list=PLLc2nQDXYMHowSZ4Lkq2jnZ0gsJL3ArAw) playlist from Alan Rodrigues. Thanks Alan!

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

## Part 2 Table of Contents

- [Intro](#intro)
- [Result](#result)

# Project

<a id="intro"></a>

## Intro

In this part we'll explore what a Terraform configuration file is, and a few concepts used within it.

<a id="result"></a>

## Result

## [Part 2: Azure Infrastructure with Terraform - Concepts when it comes to Terraform](https://www.youtube.com/watch?v=ov2of5ZCQgU&list=PLLc2nQDXYMHowSZ4Lkq2jnZ0gsJL3ArAw&index=2)

The code that will be used is defined in a Terraform configuration file. This file tells Terraform how to manage the infrastructure. In this file, blocks of code are held. These blocks are used to represent the configuration of an object. An example is given by way of a resource block:

```
resource "azurerm_resource_group" "app-grp"{
    name="app-grp"
    location="North Europe"
}
```
The resource block is used to represent the infrastructure you want to deploy. It will contain the resource type ```"azurerm_resource_group"``` and name ```"app-grp"```.

The resource type and name will become the resource identifier in the form of ```resource_type.resource_name```. 

The name ```name = "app-grp"``` and location ```location = "North Europe"``` are arguments within the resource block. This is to ensure the right property values are in place when defining the resource. You decide these arguments depending on the resource needs.

Finally you have the providers. These allow Terraform to work with external providers such as Azure or AWS. For Azure you would use an Azure provider, and for AWS an AWS provider. 


