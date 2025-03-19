# Terraform - Azure - Part 1: Azure Infrastructure with Terraform - What and Why Terraform
In this project I am going to learn to use Terraform in Azure. The reason for learning Terraform over ARM templates (or Bicep) is that Terraform can be used on other cloud platforms such as AWS and Google Cloud. I am following along with the [Azure Infrastructure with Terraform](https://www.youtube.com/playlist?list=PLLc2nQDXYMHowSZ4Lkq2jnZ0gsJL3ArAw) playlist from Alan Rodrigues. Thanks Alan!

## Project Table of Contents
- [Part 1: Azure Infrastructure with Terraform - What and Why Terraform](Part-1-Azure-Infrastructure-With-Terraform-What-and-Why-Terraform.md)
- [Part 2: Azure Infrastructure with Terraform - Concepts when it comes to Terraform](Part-2-Azure-Infrastructure-with-Terraform-Concepts-when-it-comes-to-Terraform.md)
- [Part 3: Azure Infrastructure with Terraform - Terraform workflow](Part-3-Azure-Infrastructure-with-Terraform-Terraform-workflow.md)
- [Part 4: Azure Infrastructure with Terraform - Installing Terraform](Part-4-Azure-Infrastructure-with-Terraform-Installing-Terraform.md)
- [Part 5: Azure Infrastructure with Terraform - Creating a resource group](Part-5-Azure-Infrastructure-with-Terraform-Creating-a-resource-group.md)
- [Part 6: Azure Infrastructure with Terraform - Creating an Azure Storage Account](Part-6-Azure-Infrastructure-with-Terraform-Creating-an-Azure-Storage-Account.md)
- [Part 7: Azure Infrastructure with Terraform - Terraform state](Part-7-Azure-Infrastructure-with-Terraform-Terraform-state.md)
- [Part 8: Azure Infrastructure with Terraform - Creating a container and a blob](Part-8-Azure-Infrastructure-with-Terraform-Creating-a-container-and-a-blob.md)
- [Part 9: Azure Infrastructure with Terraform - Dependencies between resources](Part-9-Azure-Infrastructure-with-Terraform-Dependencies-between-resources.md)
- [Part 10: Azure Infrastructure with Terraform - Destroying the resources](Part-10-Azure-Infrastructure-with-Terraform-Destroying-the-resources.md)
- [Part 11: Azure Infrastructure with Terraform - Using Variables](Part-11-Azure-Infrastructure-with-Terraform-Using-Variables.md)
- [Part 12: Azure Infrastructure with Terraform - Lab - Creating an Azure virtual network](Part-12-Azure-Infrastructure-with-Terraform-Lab-Creating-an-Azure-virtual-network.md)
- [Part 13: Azure Infrastructure with Terraform - Lab - Creating an Azure virtual machine](Part-13-Azure-Infrastructure-with-Terraform-Lab-Creating-an-Azure-virtual-machine.md)
- [Part 14: Azure Infrastructure with Terraform - Quick note on accessing Azure resource properties](Part-14-Azure-Infrastructure-with-Terraform-Quick-note-on-accessing-Azure-resource-properties.md)

## Part 1 Table of Contents

- [Intro](#intro)
- [Result](#result)


# Project

<a id="intro"></a>

## Intro

In this part we're going to talk about the what and why of Terraform.


<a id="result"></a>

## Result

## [Part 1: Azure Infrastructure with Terraform - What and Why Terraform](https://www.youtube.com/watch?v=lH3KT9RUEOA&list=PLLc2nQDXYMHowSZ4Lkq2jnZ0gsJL3ArAw&index=1) 


Terraform is an open-source tool that is used for provisioning and managing cloud infrastructure. 

When you create a set of resources, for example; an Azure vnet with subnet and VMs, an Azure SQL database and Storage account, you have to deploy these all by hand. By submitting a Terraform config file that is configured for the aforementioned resources, to the Terraform executable, all will be done automatically. 

One example where you would use this automation is a test environment for an application. You can deploy the necessary resources for the test environment in one go, and once you've gone through the tests and you want to delete everything, you can do so in one go also. This significantly reduces time spent on deploying all resources for the resources listed in the previous paragraph. Mind you, that list is one of the simplest environments you will come across. So the potential to save time only increases from there. 

The way it works is through IaC (Infrastructure as Code). you build the code in a matter of minutes. you do this within the Terraform configuration file. This code then tells Azure, through the Terraform interface, what resources to deploy.

An advantage of Terraform is that it works with multiple cloud platforms. Platforms like Azure, AWS, and Google Cloud. This makes the knowledge of Terraform transferable to other cloud platforms. When using Azure, you can also use ARM templates to achieve the same as Terraform. The downside of this is that ARM templates is only applicable to Azure. How Terraform is able to work with other platforms is through providers. For example, Azure will use an Azure provider, AWS an AWS provider, etc. etc.

