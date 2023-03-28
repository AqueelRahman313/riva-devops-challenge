# Solution


## Create remote backend s3 bucket

```bash
$ cd terraform/backend
$ terraform init
$ terraform apply --auto-approve
```

## Create ECS cluster with autoscaling and nginx hellow world image with terraform

```bash
$ cd terraform
$ terraform init
$ terraform apply --auto-approve
# Get the ALB url from `terraform output` and access in the browser to view hello world image
```

## Automated Deployment

1. github actions pipeline created to automate deployment of ecs cluster
2. Edit terraform/task-definition.json file  with different html body and commit
3. github actions pipeline will be triggered and ecs task definition updated 
4. Access ALB url to view the change reflected
