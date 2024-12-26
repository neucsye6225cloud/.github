# GCP Infrastructure Deployment with Terraform

Welcome to the Terraform configuration repository for deploying infrastructure on Google Cloud Platform (GCP). This README provides a detailed overview of the activated services, current configurations, and guidelines for managing the infrastructure using Terraform.

## Services Activated on GCP

Our Terraform configuration enables the following services on GCP:

- **Compute Engine API**
- **VPC (Virtual Private Cloud)**
- **Firewall**
- **Service Networking API**
- **Cloud Build API**
- **Cloud Functions API**
- **Cloud Logging API**
- **Eventarc API**
- **Cloud Pub/Sub API**
- **Cloud Run Admin API**

## Current Configuration

Here is an overview of our current infrastructure configuration:

- **Region**: `us-east1`
- **Zone**: `us-east1-b`
- **IP CIDR Range for Web Application**: `69.4.20.0/24` -> `10.1.0.0/24`
- **IP CIDR Range for Database**: `4.20.69.0/24` -> `10.2.0.0/24`
- **Firewall Rules**: Allow traffic to port `8000`
- **Compute Instance Custom Image**: `webapp-centos-stream-8-a4-v1-20240227204431`

## Managing Infrastructure with Terraform

To manage the infrastructure, follow these steps:

1. **Initialize Terraform**
   - Execute `terraform init` to initialize the Terraform modules and prepare the working directory.

2. **Validate Configuration**
   - Run `terraform validate` to check the syntax and consistency of the configuration files.

3. **Plan Infrastructure Changes**
   - Use `terraform plan` to preview the changes that Terraform will apply to the infrastructure based on the current configuration.

4. **Apply Changes**
   - Execute `terraform apply` to implement the changes defined in the configuration files. This command will create or update the resources on GCP.
  
## Key Takeaways and Improvements

- **IP Range Selection**: Proper selection of IP ranges is essential for maintaining connectivity with GCP's internal services.
- **Network Segmentation**: Adjusted subnet configurations to avoid conflicts and improve network segmentation.
- **Enhanced Connectivity**: Implemented VPC peering and Serverless VPC connectors to facilitate better service connectivity.
- **Infrastructure Image Path**: Ensured consistency by updating the image path for building new infrastructure.
- **Cloud SQL Security**: Enhanced the security of Cloud SQL instances by configuring them with private IP addresses.
- **Connectivity Solutions**: Utilized Private Service Access (PSA) and VPC peering for secure and private intra-VPC connections.
- **Private Service Connect (PSC)**: Configured PSC for secure private connectivity within the VPC network.
- **Firewall Tagging**: Improved network security by applying firewall rules based on tags.

By following these best practices and continuous learning, we aim to maintain a secure and efficient infrastructure on Google Cloud Platform.

  
