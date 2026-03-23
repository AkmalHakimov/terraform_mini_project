# terraform-basics

A hands-on introduction to Terraform using AWS. This folder covers the core concepts you need to get comfortable with Terraform before moving on to more complex infrastructure — things like writing your first configuration, understanding state, and spinning up an EC2 instance from scratch.

It's not meant to be production-ready. It's meant to be readable, tweakable, and a good place to start.

---

## What's covered

The configurations here walk through the foundational Terraform workflow on AWS — defining a provider, writing resource blocks, working with variables and outputs, and understanding what happens when you run `plan`, `apply`, and `destroy`. The main resource being provisioned is an EC2 instance.

---

## Prerequisites

Before you run anything, make sure you have:

- [Terraform](https://developer.hashicorp.com/terraform/install) installed (v1.0 or later is fine)
- An AWS account with credentials configured locally
- The AWS CLI set up, or your credentials exported as environment variables

```bash
export AWS_ACCESS_KEY_ID="your-access-key"
export AWS_SECRET_ACCESS_KEY="your-secret-key"
export AWS_DEFAULT_REGION="us-east-1"
```

---

## Getting started

Clone the repo and navigate to this folder:

```bash
git clone https://github.com/AkmalHakimov/terraform_mini_project.git
cd terraform_mini_project/terraform-basics
```

Initialize Terraform to download the AWS provider:

```bash
terraform init
```

Preview what Terraform is going to create:

```bash
terraform plan
```

Apply the configuration to provision the resources:

```bash
terraform apply
```

When you're done and want to tear everything down:

```bash
terraform destroy
```

---

## Project structure

```
terraform-basics/
├── main.tf          # Provider config and resource definitions
├── variables.tf     # Input variables
├── outputs.tf       # Output values after apply
└── terraform.tfvars # Variable values (if present)
```

---

## A note on costs

This provisions real AWS resources, so you may incur charges. EC2 instances within the free tier (t2.micro or t3.micro) are covered for new accounts, but it's always worth running `terraform destroy` when you're done experimenting.

---

## Part of a larger project

This folder is one piece of the [terraform_mini_project](https://github.com/AkmalHakimov/terraform_mini_project) repo, which covers progressively more complex Terraform concepts across multiple directories.
