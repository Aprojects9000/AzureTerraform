# Terraform - Azure - Part 4: Azure Infrastructure with Terraform - Installing Terraform
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

## Part 4 Table of Contents

- [Intro](#intro)
- [Result](#result)

# Project

<a id="intro"></a>

## Intro

In this part we're going to download and install Terraform.

<a id="result"></a>

## Result

## [Part 4: Azure Infrastructure with Terraform - Installing Terraform](https://www.youtube.com/watch?v=8I12jCmvz-0&list=PLLc2nQDXYMHowSZ4Lkq2jnZ0gsJL3ArAw&index=4)

This is a follow along to download and install Terraform. Want to follow along? Click on the title link.

The steps are as follows:

1. Download the correct Terraform .exe file from [here](https://developer.hashicorp.com/terraform/install). 
2. Set up a new app directory (or use an existing one. I chose to make a new one just because I haven't done this before) in a location of your choice. I chose to make an app directory on my D:\ partition. 
3. In case of a new app directory, add the directory to the path variable. 
4. Unpack the Terraform.zip file in the new directory.
5. Place the unpacked Terraform.exe file from the unpacked map to the (new) app directory.
5. Download, install & or open VSCode. I have it installed so will skip the download and install process.
6. Create a tmp directory on a partition of your choice where the configuration files will be stored.
7. Open a folder in VSCode, under the file menu, and choose the tmp directory. 
8. Go to the extension marketplace, found on the left hand side in VSCode, and download HashiCorp Terraform to extend the functionality of VSCode. Also download Azure Terraform, as this will help to work with Azure from Terraform.
9. Create a new file and choose the Terraform language. (In the video he makes a new text file and from there chooses a language. When I make a new file I cannot find the Terraform language.)
10. Save the file to a name of your choice. I followed along and called it 'main'.
11. The Terraform configuration file has been set up and is ready to be made into a usable configuration file.

In the following part we'll continue building the configuration file. 
