# Glue Workflow
This module creates a Glue Workflow that can be found at `"${var.project-name}-${var.module-name}"`

## Example Usage
```terraform
module "data-workflow" {
  source = "git@github.com:data-derp/terraform-modules.git//glue-workflow"

  project-name = var.project-name
  module-name = var.module-name
}
```