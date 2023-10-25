# Changelog


# v0.5.1
_Released Apr 6, 2023_
## What's Changed
* [CORE-669] Add permission to create ingress by @eak12913 in https://github.com/gruntwork-io/terraform-kubernetes-namespace/pull/27

**Full Changelog**: https://github.com/gruntwork-io/terraform-kubernetes-namespace/compare/v0.5.0...v0.5.1
<br>

# v0.5.0
_Released Feb 21, 2022_
## Description

**Terraform 1.1 upgrade**: We have verified that this repo is compatible with Terraform `1.1.x`! 
  - From this release onward, we will only be running tests with Terraform `1.1.x` against this repo, so we recommend updating to `1.1.x` soon! 
  - We have also updated the minimum required version of Terraform to `1.0.0`. While our repos might continue to be compatible with pre-1.0.0 version of Terraform, we are no longer making any guarantees of that.
  - Once all Gruntwork repos have been upgraded to work with `1.1.x`, we will publish a migration guide with a version compatibility table and announce it all via the Gruntwork Newsletter.


## Links

- https://github.com/gruntwork-io/terraform-kubernetes-namespace/pull/10
- https://github.com/gruntwork-io/terraform-kubernetes-namespace/pull/11
- https://github.com/gruntwork-io/terraform-kubernetes-namespace/pull/12
- https://github.com/gruntwork-io/terraform-kubernetes-namespace/pull/13
- https://github.com/gruntwork-io/terraform-kubernetes-namespace/pull/14
- https://github.com/gruntwork-io/terraform-kubernetes-namespace/pull/15
- https://github.com/gruntwork-io/terraform-kubernetes-namespace/pull/17
<br>

# v0.4.0
_Released Jul 28, 2021_
## Description

- **Terraform 1.0 upgrade**: We have verified that this repo is compatible with Terraform `1.0.x`! 
    - From this release onward, we will only be running tests with Terraform `1.0.x` against this repo, so we recommend updating to `1.0.x` soon! 
    - To give you more time to upgrade, for the time being, all modules will still support Terraform `0.15.1` and above, as that version has several features in it (`required_providers` with `source` URLs) that make it more forwards compatible with `1.0.x`. 
    - Once all Gruntwork repos have been upgrade to work with `1.0.x`, we will publish a migration guide with a version compatibility table and announce it all via the Gruntwork Newsletter.


## Links

- https://github.com/gruntwork-io/terraform-kubernetes-namespace/pull/9
<br>

# v0.3.1
_Released Jul 9, 2021_
## Description
- Add Terraform validation test that will scan the entire repo for Terraform modules and run terraform init and terraform validate on each.
- Replace `go fmt` in the pre-commit configuration file with `goimports`
## Links
- https://github.com/gruntwork-io/terraform-kubernetes-namespace/pull/8
- https://github.com/gruntwork-io/terraform-kubernetes-namespace/pull/7
<br>

# v0.3.0
_Released May 25, 2021_
## Description

- **Terraform 0.15 upgrade**: We have verified that this repo is compatible with Terraform `0.15.x`! 
    - From this release onward, we will only be running tests with Terraform `0.15.x` against this repo, so we recommend updating to `0.15.x` soon! 
    - To give you more time to upgrade, for the time being, all modules will still support Terraform `0.12.26` and above, as that version has several features in it (`required_providers` with `source` URLs) that make it more forwards compatible with `0.15.x`. 
    - Once all Gruntwork repos have been upgrade to work with `0.15.x`, we will publish a migration guide with a version compatibility table and announce it all via the Gruntwork Newsletter.

## Links

- https://github.com/gruntwork-io/terraform-kubernetes-namespace/pull/5
<br>

# v0.2.0
_Released Apr 13, 2021_
## Description

- **Terraform 0.14 upgrade**: We have verified that this repo is compatible with Terraform `0.14.x`! 
    - From this release onward, we will only be running tests with Terraform `0.14.x` against this repo, so we recommend updating to `0.14.x` soon! 
    - To give you more time to upgrade, for the time being, all modules will still support Terraform `0.12.26` and above, as that version has several features in it (`required_providers` with `source` URLs) that make it more forwards compatible with `0.14.x`. 
    - Once all Gruntwork repos have been upgrade to work with `0.14.x`, we will publish a migration guide with a version compatibility table and announce it all via the Gruntwork Newsletter.

## Links

- https://github.com/gruntwork-io/terraform-kubernetes-namespace/pull/4
<br>

# v0.1.1
_Released Jan 7, 2021_
## Description

Update README links to reflect new repo.

## Special thanks

Special thanks to @dcfsc for their contribution!

## Links

- https://github.com/gruntwork-io/terraform-kubernetes-namespace/pull/2
<br>

# v0.1.0
_Released Dec 15, 2020_
## Description

This repo is a port of the Namespace modules from `terraform-kubernetes-helm`. The following modules were ported over:

- `k8s-namespace` => `namespace`
- `k8s-namespace-roles` => `namespace-roles`
- `k8s-service-account` => `service-account`

These are straight ports for the most part, with the following changes:

- The modules now work with terraform 0.13.x.
- Resource rename: `rbac_tiller_metadata_access_role` => `rbac_helm_metadata_access_role`
- Resource rename: `rbac_tiller_resource_access_role` => `rbac_helm_resource_access_role`

## Migration guide

To migrate to this repo from `terraform-kubernetes-helm`, do the following:

- Change source references to point to this repo:
    - `source = "git::https://github.com/gruntwork-io/terraform-kubernetes-helm.git//modules/k8s-namespace?ref=v0.6.1"` => `source = "git::https://github.com/gruntwork-io/terraform-kubernetes-namespace.git//modules/namespace?ref=v0.1.0"`
    - `source = "git::https://github.com/gruntwork-io/terraform-kubernetes-helm.git//modules/k8s-namespace-roles?ref=v0.6.1"` => `source = "git::https://github.com/gruntwork-io/terraform-kubernetes-namespace.git//modules/namespace-roles?ref=v0.1.0"`
    - `source = "git::https://github.com/gruntwork-io/terraform-kubernetes-helm.git//modules/k8s-service-account?ref=v0.6.1"` => `source = "git::https://github.com/gruntwork-io/terraform-kubernetes-namespace.git//modules/service-account?ref=v0.1.0"`

- Change any references to `rbac_tiller_metadata_access_role` and `rbac_tiller_resource_access_role` to `rbac_helm_resource_access_role` and `rbac_helm_resource_access_role`.

- Note that the RBAC roles for Tiller will be recreated under the new name. If you have any RBAC Role bindings that use the tiller based names, you will want to update all the role bindings to remove references to the Tiller roles first, before updating this module. Then, you can add back in the new roles after deploying the update.
<br>

