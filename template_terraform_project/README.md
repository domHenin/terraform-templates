# Using Terraform to Create an Environment

# Overview

Found new infrastructure to build. This will allow new hands on experience with different AWS Services using Terraform.

-----


## Getting Started


-----


### Guides
- [Terraform Registry for Building AWS Architecture](https://registry.terraform.io/providers/hashicorp/aws/latest/docs)
- [Automate infrastructure on any cloud with Terraform](https://www.terraform.io/)
- [Start Building on AWS Today](https://aws.amazon.com/)
- [AWS Whitepapers & Guides](https://aws.amazon.com/whitepapers/)
-----

### AWS Profile
The following will connect to the proper credentials in order to build infrastructure

```sh
aws profile -configure <name-of-profile>
AWS_PROFILE=<name-of-profile> terraform <command>
```

---

### Initializing Terraform

The following will initialize the local [terraform][tfhome] configuration without
creating a bucket for storing state data.

```sh
cd ./<terraform-directory>
terraform init
terraform validate
```


-----

### Running Terraform

Run the following to ensure ***terraform*** will only perform the expected
actions:

```sh
AWS_PROFILE=<name-of-profile> terraform plan
AWS_PROFILE=<name-of-profile> terraform apply
```

### Tearing Down the Terraformed Infrastructure

Run the following to verify that ***terraform*** will only impact the expected
nodes and then tear down the cluster.

```sh
AWS_PROFILE=<name-of-profile> terraform plan
AWS_PROFILE=<name-of-profile> terraform destroy
```
----

### Documentation

------

### Module Structure

```sh
terraform-build/
├─ diagram/
├─ modules/
│  ├─ aws/
│  │  ├─ network-base/
│  │  ├─ compute-base/
├─ main.tf
├─ variables.tf
├─ outputs.tf
├─ README.md
├─ .gitignore


```

----

### Appendix

- [ASCII Tree Generator -- Module Structure](https://ascii-tree-generator.com/)

----
[tfhome](https://www.terraform.io)
[tfdocs](https://registry.terraform.io/providers/hashicorp/aws/latest/docs)