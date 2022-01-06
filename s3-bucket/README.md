# S3 Bucket
This creates bucket.

## Example Usage
```terraform
module "s3-bucket" {
  source = "git@github.com:data-derp/terraform-modules.git//s3-bucket"

  bucket-name = "${var.project-name}-${var.module-name}"
  force-destroy = true
}
```