# Using Terraform to Provision EC2 Instance on AWS, Azure, or Google Cloud

## Theory

### 1. What is Terraform?

Terraform is an open-source infrastructure as code (IaC) software tool created by HashiCorp. It allows users to define and provision data center infrastructure using a high-level configuration language called HashiCorp Configuration Language (HCL) or optionally JSON.

With Terraform, you can manage infrastructure across various cloud providers (such as AWS, Azure, Google Cloud, etc.) as well as on-premises infrastructure. It provides a way to define, manage, and version infrastructure in a declarative manner, enabling automation and reproducibility.

### 2. Step-by-step Screenshots to Install and Configure Terraform

Below are the steps to install and configure Terraform:

1. **Download Terraform**: Visit the [Terraform website](https://www.terraform.io/downloads.html) and download the appropriate version for your operating system (Windows, Linux, macOS).

2. **Extract the Archive**: After downloading, extract the Terraform archive to a directory of your choice. For example, on Linux or macOS, you can use the following command:
   ```
   $ unzip terraform.zip -d /usr/local/bin/
   ```

3. **Verify Installation**: To ensure Terraform is installed correctly, open a terminal or command prompt and run:
   ```
   $ terraform version
   ```
   This command should display the installed Terraform version.

4. **Configure Access Keys**: If you plan to provision resources on cloud providers like AWS, Azure, or Google Cloud, you need to configure access keys or service account credentials. This can typically be done by setting environment variables or using a configuration file provided by the respective cloud provider.

5. **Initialize Terraform**: Once Terraform is installed and configured with access credentials, navigate to your Terraform configuration directory containing your `.tf` files and run:
   ```
   $ terraform init
   ```
   This command initializes Terraform and downloads any necessary plugins for providers specified in your configuration files.

6. **Write Terraform Configuration**: Write your Terraform configuration files (typically with a `.tf` extension) defining the infrastructure resources you want to provision. This includes specifying the provider (e.g., AWS, Azure, Google Cloud), resource types (e.g., EC2 instance), and their configurations.

7. **Plan and Apply Changes**: After writing your Terraform configuration, you can preview the changes Terraform will make by running:
   ```
   $ terraform plan
   ```
   This command shows a summary of the actions Terraform will take. Once you are satisfied with the plan, apply the changes by running:
   ```
   $ terraform apply
   ```
   Terraform will then create, update, or delete resources as necessary to match your configuration.

8. **Destroy Resources (Optional)**: If you want to remove the resources provisioned by Terraform, you can run:
   ```
   $ terraform destroy
   ```
   This command will prompt you to confirm the destruction of resources before proceeding.

## Terraform Configuration Example

Please refer to the `main.tf` file in this repository for a sample Terraform configuration that provisions an EC2 instance on AWS, Azure, or Google Cloud. Additionally, input and output variable files (`input.tf` and `outputs.tf`) are provided to demonstrate the usage of variables in Terraform configurations.

Feel free to modify the configuration files according to your requirements and cloud provider credentials.

--- 

This README provides an overview of using Terraform to provision infrastructure and outlines the installation process along with theoretical insights. For detailed examples and configurations, please refer to the accompanying files in the repository.
