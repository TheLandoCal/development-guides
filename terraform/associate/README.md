# HashiCorp Certified: Terraform Associate

TBD Terraform Associate exam overview

See [HashiCorp Learn: Terraform Associate Prep](https://learn.hashicorp.com/collections/terraform/certification) for the official preperation guide.

# Table of Contents

TBD Table of Contents

## Topics

TBD Example Topics/Objectives

## Sample Questions

Below are sample questions (from [HashiCorp Learn](https://learn.hashicorp.com/tutorials/terraform/associate-questions?in=terraform/certification)) with additional explanation about the correct answer and where to find its justifications in the Terraform documentation.

1.  Usernames and passwords referenced in the Terraform code, even as variables, will end up in plain text in the state file.

    - True
    - False

    <details>
    <summary>Answer</summary>

    **True**

    <h3>Explanation</h3>
    TBD
    <h3>Source</h3>
    TBD
    </details>

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
    TBD
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
    TBD
    </details>

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
    TBD
    </details>

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
    TBD
    </details>

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
    TBD
    </details>
