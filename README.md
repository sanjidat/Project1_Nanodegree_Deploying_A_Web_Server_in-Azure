# Project1_Nanodegree_Deploying_A_Web_Server_in-Azure

Azure Infrastructure Operations Project: Deploying a scalable IaaS web server in Azure.

## Introduction

For this project, you will write a Packer template and a Terraform template to deploy a customizable, scalable web server in Azure.

### Getting Started

1. Clone this repository
2. Create your infrastructure as code
3. Update this README to reflect how someone would use your code.

### Dependencies
 
1. Create an Azure Account
2. Install the Azure command line interface
3. Install Packer
4. Install Terraform

### Instructions

#### Step 1: Policy Deploy:
Create a policy that ensures all indexed resources are tagged. Create the policy using Azure CLI. After creating policy run "policy assignment list" command. 

#### Step 2: Building Packer Template
Create a server image using Packer template 'server.json'. Run the command "packer build" in order to create a server image. Using the command "az image list" it is possible to access the image. In order to remove the image from the resource group run the command 
"az image delete -g packer-rg -n <name>".

#### Step3: Creating the infrastructure using terraform and packer.
The infrastructure is deployed using terraform and packer template in Azure. There are two files- main.tf in which all the resources are created and var.tf in which variables are created. The var.tf file can be customized according to the user information, for example- value of count, resource group name, location etc. Following are he commands for terraform template.

•	Run the command "terraform init" to get started. 
 
 
•	Run "terraform plan" to vie the resources that will be created. Also run the command "terraform plan -out <filename>" to save it in a file. 
 
 
•	Run "terraform apply" to apply plan and deploy infrastructure.
 
 
•	Run "terraform show" to see the deployed infrastructure.
 
 
•	Run "terraform destroy" to take down the created infrastructure. 
 
 
•	Run again "terraform show" to verify the previous command.


Output
A Linux 18.04 LTS Virtual Machine is deployed in Microsoft Azure.  
