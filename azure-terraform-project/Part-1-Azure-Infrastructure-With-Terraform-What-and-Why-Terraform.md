# Terraform - Azure - Part 1: Azure Infrastructure with Terraform - What and Why Terraform
In this project I am going to learn to use Terraform in Azure. The reason for learning Terraform over ARM templates (or Bicep) is that Terraform can be used on other cloud platforms such as AWS and Google Cloud. I am following along with the [Azure Infrastructure with Terraform](https://www.youtube.com/playlist?list=PLLc2nQDXYMHowSZ4Lkq2jnZ0gsJL3ArAw) playlist from Alan Rodrigues. Thanks Alan.

## Project Table of Contents
- [Part 1: Azure Infrastructure with Terraform - What and Why Terraform](Part-1-Azure-Infrastructure-With-Terraform-What-and-Why-Terraform.md)
- [Part 2: Azure Infrastructure with Terraform - Concepts when it comes to Terraform](Part-2-Azure-Infrastructure-with-Terraform-Concepts-when-it-comes-to-Terraform.md)
- [Part 3: Azure Infrastructure with Terraform - Terraform workflow](Part-3-Azure-Infrastructure-with-Terraform-Terraform-workflow.md)
- [Part 4: Azure Infrastructure with Terraform - Installing Terraform](Part-4-Azure-Infrastructure-with-Terraform-Installing-Terraform.md)
- [Part 5: Azure Infrastructure with Terraform - Creating a resource group](Part-5-Azure-Infrastructure-with-Terraform-Creating-a-resource-group.md)

## Part 1 Table of Contents

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

## [Part 1: Azure Infrastructure with Terraform - What and Why Terraform](https://www.youtube.com/watch?v=lH3KT9RUEOA&list=PLLc2nQDXYMHowSZ4Lkq2jnZ0gsJL3ArAw&index=1) 


Here Alan explains the what and the why of Terraform. 

Terraform is an open-source tool that is used for provisioning and managing cloud infrastructure. 

When you create a set of resources, for example; an Azure vnet with subnet and VMs, an Azure SQL database and Storage account, you have to deploy these all by hand. By submitting a Terraform config file that is configured for the aforementioned resources, to the Terraform executable, all will be done automatically. 

One example where you would use this automation is a test environment for an application. You can deploy the necessary resources for the test environment in one go, and once you've gone through the tests and you want to delete everything, you can do so in one go also. This significantly reduces time spent on deploying all resources for the resources listed in the previous paragraph. Mind you, that list is one of the simplest environments you will come across. So the potential to save time only increases from there. 

The way it works is through IaC (Infrastructure as Code). you build the code in a matter of minutes. you do this within the Terraform configuration file. This code then tells Azure, through the Terraform interface, what resources to deploy.

An advantage of Terraform is that it works with multiple cloud platforms. Platforms like Azure, AWS, and Google Cloud. This makes the knowledge of Terraform transferable to other cloud platforms. When using Azure, you can also use ARM templates to achieve the same as Terraform. The downside of this is that ARM templates is only applicable to Azure. How Terraform is able to work with other platforms is through providers. For example, Azure will use an Azure provider, AWS an AWS provider, etc. etc.

