# Terraform - Azure - Part 4: Azure Infrastructure with Terraform - Installing Terraform
In this project I am going to learn to use Terraform in Azure. The reason for learning Terraform over ARM templates (or Bicep) is that Terraform can be used on other cloud platforms such as AWS and Google Cloud. I am following along with the [Azure Infrastructure with Terraform](https://www.youtube.com/playlist?list=PLLc2nQDXYMHowSZ4Lkq2jnZ0gsJL3ArAw) playlist from Alan Rodrigues. Thanks Alan.

## Project Table of Contents
- [Part 1: Azure Infrastructure with Terraform - What and Why Terraform](Part-1-Azure-Infrastructure-With-Terraform-What-and-Why-Terraform.md)
- [Part 2: Azure Infrastructure with Terraform - Concepts when it comes to Terraform](Part-2-Azure-Infrastructure-with-Terraform-Concepts-when-it-comes-to-Terraform.md)
- [Part 3: Azure Infrastructure with Terraform - Terraform workflow](Part-3-Azure-Infrastructure-with-Terraform-Terraform-workflow.md)
- [Part 4: Azure Infrastructure with Terraform - Installing Terraform](Part-4-Azure-Infrastructure-with-Terraform-Installing-Terraform.md)
- [Part 5: Azure Infrastructure with Terraform - Creating a resource group](Part-5-Azure-Infrastructure-with-Terraform-Creating-a-resource-group.md)

## Part 4 Table of Contents

- [Key-terms](#key-terms)
- [Used sources](#used-sources)
- [Result](#result)

# Project

<a id="key-terms"></a>

## Key-terms

**Terraform:**  Terraform is an opensource tool used for provisioning and managing cloud infrastructure. By using IaC (Infrastructure as Code) you can simplify the deployment of resources by automating the process instead of having to create all your resources by hand.

**IaC (Infrastructure as Code):** Infrastructure as Code (IaC) is the managing and provisioning of infrastructure through code instead of through manual processes.

**ARM templates:** ARM templates offer the same service as Terraform, the difference being it is native to Microsoft Azure. 

**Terraform configuration file:** This tells Terraform how to manage the infrastructure.

**Blocks:** These are used to represent the configuration of an object. They are found within the Terraform configuration file.

**Resource block:** This is a block used to represent the infrastructure you want to deploy. This will contain the resource type, the name, and the location. The resource type and the name become the resource identifier in the format of ```resource_type.resource_name```. The name and location are arguments within the resource block.

**Provider:** These allow Terraform to work with external providors like Azure, or AWS.

**Azure Active Directory (Now called Microsoft Entra ID):** The Azure Active Directory is your Multicloud identity and access management provider. Through it you can manage who has access to your apps and resources in the cloud. It can also be used to manage your on-premises environment. This is done by creating user identities.

<a id="used-sources"></a>

## Used sources

[1. The Azure Infrastructure with Terraform project of Alan Rodrigues](https://www.youtube.com/playlist?list=PLLc2nQDXYMHowSZ4Lkq2jnZ0gsJL3ArAw)

[2. How to create a table of contents](https://stackoverflow.com/questions/11948245/markdown-to-create-pages-and-table-of-contents)

[3. What is Azure Active Directory (Now called Microsoft Entra ID)?](https://www.microsoft.com/en-us/security/business/identity-access/microsoft-entra-id)

[4. What is IaC (Infrastructure as Code)?](https://redhat.com/en/topics/automation/what-is-infrastructure-as-code-iac)

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

In the following video we'll continue building the configuration file. 
