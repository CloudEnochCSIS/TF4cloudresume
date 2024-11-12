# DigitalOcean Terraform Project

This project uses Terraform to provision and manage infrastructure on DigitalOcean. The resources include a Droplet, a domain, a DNS record, and a firewall.

## Prerequisites

- [Terraform](https://www.terraform.io/downloads.html) installed
- A DigitalOcean account
- A DigitalOcean API token

## Setup

1. **Clone the repository**:
    ```sh
    git clone https://github.com/CloudEnochCSIS/TF4cloudresume.git
    cd TF4cloudresume
    ```

2. **Create a `terraform.tfvars` file**:
    ```sh
    touch terraform.tfvars
    ```

3. **Add your DigitalOcean API token to `terraform.tfvars`**:
    ```sh
    do_token = "your_digitalocean_api_token"
    ```

## Usage

1. **Initialize Terraform**:
    ```sh
    terraform init
    ```

2. **Plan the infrastructure**:
    ```sh
    terraform plan
    ```

3. **Apply the configuration**:
    ```sh
    terraform apply
    ```

## Resources

- **DigitalOcean Droplet**: A virtual machine instance named "cloud-resume".
- **DigitalOcean Domain**: A domain named "cloudenoch.com".
- **DigitalOcean DNS Record**: An A record pointing the domain to the Droplet's IPv4 address.
- **DigitalOcean Firewall**: A firewall with specific inbound and outbound rules.

## Inbound Rules

- **SSH (port 22)**: Open to all IP addresses.
- **HTTP (port 80)**: Open to all IP addresses.
- **HTTPS (port 443)**: Open to all IP addresses.

## Outbound Rules

- **TCP (ports 1-65535)**: Open to all IP addresses.
- **UDP (ports 1-65535)**: Open to all IP addresses.

## Cleanup

To destroy the infrastructure, run:
```sh
terraform destroy
