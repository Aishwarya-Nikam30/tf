## Basic Terraform Workflow

### Write Configuration
Define infrastructure in `.tf` files using HCL.

### Initialize (`terraform init`)
Initialize the working directory by downloading the necessary provider plugins.

### Validate (`terraform validate`)
Check whether the configuration is valid.

### Plan (`terraform plan`)
Preview the changes Terraform will make without applying them.

### Apply (`terraform apply`)
Apply the changes to reach the desired infrastructure state.

### Destroy (`terraform destroy`)
Remove all the infrastructure managed by Terraform.

---

## Common Terraform Commands

| Command               | Description                                 |
|-----------------------|---------------------------------------------|
| `terraform init`      | Initialize the working directory.          |
| `terraform validate`  | Validate the configuration.                |
| `terraform plan`      | Preview changes before applying.           |
| `terraform apply`     | Apply the changes.                         |
| `terraform destroy`   | Destroy all managed infrastructure.        |

---

## Terraform Best Practices

- **Use Remote Backend for State Files**  
  Always store `terraform.tfstate` in a remote backend like **S3** with **DynamoDB** locking to avoid losing important data.

- **Always Version Control**  
  Save `.tf` files in a version control system like **Git** to track changes and collaborate easily.

- **Use Variables and Outputs Wisely**  
  Keep your configurations **modular**, **reusable**, and easy to maintain.

- **Write Modular Code**  
  Break down your Terraform code into **modules** to promote reusability and scalability.

- **Enable State Locking**  
  Prevent concurrent operations on the same infrastructure by enabling **state locking**.

- **Keep Sensitive Data Secure**  
  Never hardcode secrets or passwords. Use **environment variables**, **Vault**, or other secret management tools.

- **Format and Validate Code**  
  Always run:
  ```bash
  terraform fmt
  terraform validate
