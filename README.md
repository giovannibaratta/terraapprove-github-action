# TerraApprove action

The TerraApprove action provides an easy way to use [TerraApprove](https://giovannibaratta.github.io/TerraApprove/) in your GitHub Actions workflow.

## Usage

The action needs 2 options to be set:
* `tf_code_dir`: the directory where the Terraform code is located
* `tf_plan_json_file`: the path to the Terraform plan JSON file

Additionally `mode` can be set to change the beahviour of the validator.