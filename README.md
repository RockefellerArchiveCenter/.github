# Organization GitHub Workflows & Documentation

This repository provides **reusable GitHub Actions workflow templates**
and documentation for use across repositories in the RAC GitHub organization.

------------------------------------------------------------------------

## Repository Structure

    .github/
    └── workflow-templates/
        └── rotate_keys.yml

-   **`workflow-templates/`**\
    Contains reusable basic GitHub Actions workflow templates that can be
    imported into other organizational repositories as starting templates.

------------------------------------------------------------------------

## Workflow Templates

### `rotate_keys`

Rotates AWS IAM access keys by invoking a Lambda function.

**What it does:** 
- Assumes an AWS role using credentials stored in
GitHub Secrets 
- Calls a Lambda function responsible for rotating IAM
access keys 
- Optionally stores newly rotated credentials in AWS SSM
Parameter Store

------------------------------------------------------------------------

## Adding New Workflow Templates

To add a new reusable workflow:

1.  Create a new `.yml` file in `workflow-templates/`
2.  Ensure it is:
    -   Parameterized (no hardcoded environment values)
3.  Update this README with a new description of the template
