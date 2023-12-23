# TerraApprove action

The TerraApprove action provides an easy way to use [TerraApprove](https://giovannibaratta.github.io/TerraApprove/) in your GitHub Actions workflow.

## Usage

The action needs 2 options to be set:
* `tf_code_dir`: the directory where the Terraform code is located
* `tf_plan_json_file`: the path to the Terraform plan JSON file

```yaml
...
steps:
  - name: TerraApprove
    id: terraapprove
    uses: giovannibaratta/terraapprove-github-action@v0.0.8
    with:
      tf_code_dir: example-01
      tf_plan_json_file: example-01/plan.json

  - name: TerraApprove output
    run: |
      echo "Approval required: ${{ steps.terraapprove.outputs.approval_required }}"
```

Additionally `mode` can be set to change the beahviour of the validator.

## Examples

A repository is avaiable [here](https://github.com/giovannibaratta/terraapprove-github-action-examples) with a complete examples.