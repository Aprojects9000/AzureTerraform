# Terraform - Azure - Part 3: Azure Infrastructure with Terraform - Terraform workflow
In this project I am going to learn to use Terraform in Azure. The reason for learning Terraform over ARM templates (or Bicep) is that Terraform can be used on other cloud platforms such as AWS and Google Cloud. I am following along with the [Azure Infrastructure with Terraform](https://www.youtube.com/playlist?list=PLLc2nQDXYMHowSZ4Lkq2jnZ0gsJL3ArAw) playlist from Alan Rodrigues. Thanks Alan.

## Project Table of Contents
- [Part 1: Azure Infrastructure with Terraform - What and Why Terraform](Part-1-Azure-Infrastructure-With-Terraform-What-and-Why-Terraform.md)
- [Part 2: Azure Infrastructure with Terraform - Concepts when it comes to Terraform](Part-2-Azure-Infrastructure-with-Terraform-Concepts-when-it-comes-to-Terraform.md)
- [Part 3: Azure Infrastructure with Terraform - Terraform workflow](Part-3-Azure-Infrastructure-with-Terraform-Terraform-workflow.md)
- [Part 4: Azure Infrastructure with Terraform - Installing Terraform](Part-4-Azure-Infrastructure-with-Terraform-Installing-Terraform.md)
- [Part 5: Azure Infrastructure with Terraform - Creating a resource group](Part-5-Azure-Infrastructure-with-Terraform-Creating-a-resource-group.md)

## Part 3 Table of Contents

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


