# Terraform - Azure - Part 3: Azure Infrastructure with Terraform - Terraform workflow
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

## Part 3 Table of Contents

- [Intro](#intro)
- [Result](#result)

# Project

<a id="intro"></a>

## Intro

In this part we're going to learn the general workflow when using a Terraform configuration file. 

<a id="result"></a>

## Result

## [Part 3: Azure Infrastructure with Terraform - Terraform workflow](https://www.youtube.com/watch?v=Puw5zDFgZI0&list=PLLc2nQDXYMHowSZ4Lkq2jnZ0gsJL3ArAw&index=3)

In this video Alan describes the Terraform workflow. It is a 4 step workflow that goes as follows:

First there are some steps that come before the workflow steps. I'll list them below

1.   The first step consists of creating a Terraform config file. Here you mention the resources that need to be deployed. 
2.   You also need to make sure to actually have Terraform installed. This step will come in the next video. Now come the four steps in the workflow:

     1.  Perform the Terraform init command. When you do this you initialise the working directory that contains the Terraform configuration files.
     2.  Now you perform the Terraform plan command. An execution plan will be created that will define the changes Terraform will make to your infrastructure. This will be based on the config file.
     3.  This is where you perform the Terraform apply command. The actions in the Terraform plan will be executed.
     4.  If you want to destroy your infrastructure, this is where the Terraform destroy command comes in. All infrastructure objects created through the config file will now be destroyed.  

In [Part 5](Part-5-Azure-Infrastructure-with-Terraform-Creating-a-resource-group.md) we'll put these steps into practice. 


