# Setup terraform

Setup terraform by:
  1. Downloading required version if needed
  2. Initializing it
## Inputs

### `terraform-version`

**Required** Terraform version. Default `"0.14.0"`.
### `workspace-key-prefix`

**Required** Path to the state file inside the S3 Bucket. Default `"preproduction"`.

## Example usage

```yaml
- uses: gogaille/setup-terraform
  env:
    AWS_ACCESS_KEY_ID: ${{ secrets.AWS_ACCESS_KEY_ID }}
    AWS_SECRET_ACCESS_KEY: ${{ secrets.AWS_SECRET_ACCESS_KEY }}
  with:
    terraform-version: '0.14.0'
    workspace-key-prefix: 'preproduction'
```
