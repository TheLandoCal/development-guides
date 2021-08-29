# HashiCorp Certified: Terraform Associate

TBD Terraform Associate exam overview

See [HashiCorp Learn: Terraform Associate Prep](https://learn.hashicorp.com/collections/terraform/certification) for the official preperation guide.

## Table of Contents

TBD Table of Contents

## Sample Questions

While HashiCorp provides a handful of sample questions, it is no where near enough to get a real feel for the true exam or to evaluate gaps in your Terraform knowledge. Here you'll find the official sample questions as well as questions created from the documentation that mirror the sample questions (constructed) mapped to the exam objectives (from [HashiCorp Learn](https://learn.hashicorp.com/tutorials/terraform/associate-review?in=terraform/certification#review-guide)).

- [ ] Add real questions after taking the exam

### 1: Understand Infrastructure as Code (IaC) concepts

#### 1a: Explain what IaC is

#### 1b: Describe advantages of IaC patterns

### 2: Understand Terraform's purpose (vs other IaC)

#### 2a: Explain multi-cloud and provider-agnostic benefits

#### 2b: Explain the benefits of state

### 3: Understand Terraform basics

#### 3a: Handle Terraform and provider installation and versioning

1.  Which flag is used to find more information about a Terraform command? For example, you need additional information about how to use the `plan` command. You would type: `terraform plan _____`. Type your answer in the field provided. The text field is not case-sensitive and all variations of the correct answer are accepted.

    <details>
    <summary>Answer</summary>

    - **`-h`**
    - **`-help`**
    - **`--help`**

    NOTE: See [this question](https://learn.hashicorp.com/tutorials/terraform/associate-questions?in=terraform/certification#text-match) on HashiCorp Learn for the full list of the variations that would be accepted as the correct answer.

    <h3>Explanation</h3>
    TBD
    <h3>Source</h3>
    [Basic CLI Features](https://www.terraform.io/docs/cli/commands/index.html)
    </details>

#### 3b: Describe plug-in based architecture

#### 3c: Demonstrate using multiple providers

#### 3d: Describe how Terraform finds and fetches providers

#### 3e: Explain when to use and not use provisioners and when to use local-exec or remote-exec

### 4: Use the Terraform CLI (outside of core workflow)

#### 4a: Given a scenario: choose when to use terraform fmt to format code

#### 4b: Given a scenario: choose when to use terraform taint to taint Terraform resources

#### 4c: Given a scenario: choose when to use terraform import to import existing infrastructure into your Terraform state

#### 4d: Given a scenario: choose when to use terraform workspace to create workspaces

#### 4e: Given a scenario: choose when to use terraform state to view Terraform state

#### 4f: Given a scenario: choose when to enable verbose logging and what the outcome/value is

### 5: Interact with Terraform modules

#### 5a: Contrast module source options

#### 5b: Interact with module inputs and outputs

#### 5c: Describe variable scope within modules/child modules

#### 5d: Discover modules from the public Terraform Module Registry

#### 5e: Defining module version

### 6: Navigate Terraform workflow

#### 6a: Describe Terraform workflow ( Write -> Plan -> Create )

#### 6b: Initialize a Terraform working directory (terraform init)

#### 6c: Validate a Terraform configuration (terraform validate)

#### 6d: Generate and review an execution plan for Terraform (terraform plan)

#### 6e: Execute changes to infrastructure with Terraform (terraform apply)

1.  What happens when you apply Terraform configuration? Choose _TWO_ correct answers.

    - Terraform makes any infrastructure changes defined in your configuration.
    - Terraform gets the plugins that the configuration requires.
    - Terraform updates the state file with any configuration changes it made.
    - Terraform corrects formatting errors in your configuration.
    - Terraform destroys and recreates all your infrastructure from scratch.

    <details>
    <summary>Answer</summary>

    - **Terraform makes any infrastructure changes defined in your configuration.**
    - **Terraform updates the state file with any configuration changes it made.**

    <h3>Explanation</h3>
    TBD
    <h3>Source</h3>
    [Build Infrastructure– Apply Changes](https://learn.hashicorp.com/tutorials/terraform/aws-build#create-infrastructure)
    </details>

#### 6f: Destroy Terraform managed infrastructure (terraform destroy)

### 7: Implement and maintain state

#### 7a: Describe default local backend

#### 7b: Outline state locking

#### 7c: Handle backend authentication methods

#### 7d: Describe remote state storage mechanisms and supported standard backends

#### 7e: Describe effect of Terraform refresh on state

1.  Which of the following Terraform commands will automatically refresh the state unless supplied with additional flags or arguments? Choose _TWO_ correct answers.

    - `terraform plan`
    - `terraform state`
    - `terraform apply`
    - `terraform validate`
    - `terraform output`

    <details>
    <summary>Answer</summary>

    - **`terraform plan`**
    - **`terraform apply`**

    <h3>Explanation</h3>
    TBD
    <h3>Source</h3>
    [Command: refresh](https://www.terraform.io/docs/cli/commands/refresh.html)
    </details>

#### 7f: Describe backend block in configuration and best practices for partial configurations

#### 7g: Understand secret management in state files

1.  Usernames and passwords referenced in the Terraform code, even as variables, will end up in plain text in the state file.

    - True
    - False

    <details>
    <summary>Answer</summary>

    **True**

    <h3>Explanation</h3>
    TBD
    <h3>Source</h3>
    [Sensitive Data in State](https://www.terraform.io/docs/language/state/sensitive-data.html)
    </details>

### 8: Read, generate, and modify configuration

#### 8a: Demonstrate use of variables and outputs

1.  Consider the following Terraform 0.12 configuration snippet:

    ```go
     variable "vpc_cidrs" {
         type = map
         default = {
             us-east-1 = "10.0.0.0/16"
             us-east-2 = "10.1.0.0/16"
             us-west-1 = "10.2.0.0/16"
             us-west-2 = "10.3.0.0/16"
         }
     }

     resource "aws_vpc" "shared" {
         cidr_block = _____________
     }

    ```

    How would you define the `cidr_block` for us-east-1 in the `aws_vpc` resource using a variable?

    - `var.vpc_cidrs["us-east-1"]`
    - `var.vpc_cidrs.0`
    - `vpc_cidrs["us-east-1"]`
    - `var.vpc_cidrs[0]`

    <details>
    <summary>Answer</summary>

    **`var.vpc_cidrs["us-east-1"]`**

    <h3>Explanation</h3>
    TBD
    <h3>Source</h3>
    [Input Variables > Using Input Variable Values](https://www.terraform.io/docs/language/values/variables.html#using-input-variable-values)
    </details>

1.  You have defined the values for your variables in the file `terraform.tfvars`, and saved it in the same directory as your Terraform configuration. Which of the following commands will use those values when creating an execution plan?

    - `terraform plan`
    - `terraform plan -var-file=terraform.tfvars`
    - All of the above
    - None of the above

    <details>
    <summary>Answer</summary>

    **All of the above**

    <h3>Explanation</h3>
    TBD
    <h3>Source</h3>
    [Input Variables > Variable Definitions (`.tfvars`) Files](https://www.terraform.io/docs/language/values/variables.html#variable-definitions-tfvars-files)
    </details>

#### 8b: Describe secure secret injection best practice

#### 8c: Understand the use of collection and structural types

#### 8d: Create and differentiate resource and data configuration

#### 8e: Use resource addressing and resource parameters to connect resources together

#### 8f: Use Terraform built-in functions to write configuration

#### 8g: Configure resource using a dynamic block

#### 8h: Describe built-in dependency management (order of execution based)

### 9: Understand Terraform Cloud and Enterprise capabilities

#### 9a: Describe the benefits of Sentinel, registry, and workspaces

#### 9b: Differentiate OSS and Terraform Cloud workspaces

#### 9c: Summarize features of Terraform Cloud
