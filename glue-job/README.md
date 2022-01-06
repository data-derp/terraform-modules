# Glue Job
This module creates Glue Job that can be found at `"${var.project-name}-${var.module-name}"`

## Example Usage
```terraform
module "glue-job" {
  source = "git@github.com:data-derp/terraform-modules.git//glue-job"

  project-name = var.project-name
  module-name = var.module-name
  submodule-name = "my-awesome-module"
  script-path = "my-local-path/main.py"
  additional-params = {
    "--extra-py-files":                   "s3://my-awesome-bucket/data_ingestion-0.1-py3.egg", # https://docs.aws.amazon.com/glue/latest/dg/reduced-start-times-spark-etl-jobs.html
    "--my_input_path":                    "s3://my-awesome-bucket/data-source/data.csv",
    "--my_output_path":                   "s3://my-awesome-bucket/ingested/ingested.parquet",
  }
}
```