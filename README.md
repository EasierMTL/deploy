# Deploying and Benchmarking with Terraform and Locust

The server docker image URI to load-test: `public.ecr.aws/h1c6y7g8/chinese-translation-api:latest`

## To-Dos

1. Clean up docs
   1. Add TOC
   2. Make it more specific to this repo
   3. Compile GCE and AWS specific setup instructions with Terraform.
2. Add templating to allow you to specify:
   1. The Docker image
   2. Backend vs Frontend?
   3. Update the nginx config appropriate
3. Add unit tests for each module
4. GKE/K8s support
5. Nicer install instructions (depends on the stack used for templating)

## Deploy API Server with Terraform

Make sure you have `terraform` installed and `aws` CLI configured.

- Feel free to change the `key_name` to the correct SSH key name that you want to ssh with.

```bash
cd server
terraform init
terraform plan
terraform apply
```

Clean up with:

```bash
terraform destroy
```
