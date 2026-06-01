# d2_docker

This repository contains sample Docker and Terraform resources for learning and experimentation.

## Structure

- `docker/`
  - `L1/Dockerfile` - first Dockerfile example
  - `L2/Dockerfile` - second Dockerfile example
  - `L3/docker-compose.yml` - docker-compose example
- `terraform/`
  - `providers.tf` - Terraform provider configuration
  - `ec2.tf` - EC2 instance and related resources
  - `userdata.sh` - instance user data script
  - `variables.tf` - Terraform variable declarations

## Usage

### Docker

1. Navigate to the `docker` directory.
2. Build or run individual Dockerfiles from their respective folders.
3. Use `docker-compose` for the `L3` example:

```bash
cd docker/L3
docker-compose up --build
```

### Terraform

1. Navigate to the `terraform` directory.
2. Initialize Terraform:

```bash
cd terraform
terraform init
```

3. Plan and apply:

```bash
terraform plan
terraform apply
```

## Notes

- Adjust Terraform variables and AWS credentials as needed before apply.
- Review the `userdata.sh` script before using it in production.
