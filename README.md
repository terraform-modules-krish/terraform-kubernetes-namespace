***WARNING: THIS REPO IS AN AUTO-GENERATED COPY.*** *This repo has been copied from [Gruntwork’s](https://gruntwork.io/) GitHub repositories so that you can consume it from your company’s own internal Git repositories. This copy is automatically created and updated by the `repo-copier` CLI tool. If you need to make changes to this repo, you should make the changes in a separate fork, and NOT make changes directly in this repo, as otherwise, the `repo-copier` will overwrite your changes! Please see the `repo-copier` [documentation](https://github.com/terraform-modules-krish/repo-copier) for more information on how the code is copied, how cross-references are updated, how the changelog is handled, etc.*

***

_You may find it valuable to view the following resources in the original repo. If these links give you a 404, visit https://app.gruntwork.io to gain access or email support@gruntwork.io if you need assistance._

[Home Page](https://github.com/gruntwork-io/terraform-kubernetes-namespace/) |
[Pull Requests](https://github.com/gruntwork-io/terraform-kubernetes-namespace/pulls) |
[Issues](https://github.com/gruntwork-io/terraform-kubernetes-namespace/issues) |
[Releases and Assets](https://github.com/gruntwork-io/terraform-kubernetes-namespace/releases)

_Alternatively, you can view a copied version of the resources listed above._

[Pull Requests](https://github.com/terraform-modules-krish/terraform-kubernetes-namespace/blob/main/.github/PULL_REQUESTS.md) |
[Issues](https://github.com/terraform-modules-krish/terraform-kubernetes-namespace/blob/main/.github/ISSUES.md) |
[ChangeLog](https://github.com/terraform-modules-krish/terraform-kubernetes-namespace/blob/main/.github/CHANGELOG.md)

***

<!--
:type: service
:name: Kubernetes Namespace
:description: Deploy a Kubernetes Namespace on to any Kubernetes cluster.
:icon: /_docs/ns-128.png
:category: docker-orchestration
:cloud: aws
:tags: docker, orchestration, kubernetes, containers
:license: gruntwork
:built-with: terraform
-->

# Kubernetes Namespace

[![Maintained by Gruntwork.io](https://img.shields.io/badge/maintained%20by-gruntwork.io-%235849a6.svg)](https://gruntwork.io/?ref=repo_k8s_namespace)
![Terraform Version](https://img.shields.io/badge/tf-%3E%3D1.1.0-blue.svg)

This repo contains a Module for managing [Kubernetes
Namespaces](https://kubernetes.io/docs/concepts/overview/working-with-objects/namespaces/) with
[Terraform](https://www.terraform.io).




## Features

* Deploy a Namespace from scratch
* Configure Namespaces with default RBAC roles
* Create and manage Namespace scoped Service Accounts with various access levels via RBAC




## Learn

This repo is a part of [the Gruntwork Infrastructure as Code Library](https://gruntwork.io/infrastructure-as-code-library/),
a collection of reusable, battle-tested, production ready infrastructure code. If you've never used the Infrastructure as Code Library
before, make sure to read [How to use the Gruntwork Infrastructure as Code Library](https://gruntwork.io/guides/foundations/how-to-use-gruntwork-infrastructure-as-code-library/)!

### Core concepts

* [What is a Namespace?](https://github.com/terraform-modules-krish/terraform-kubernetes-namespace/blob/main/modules/namespace/README.md#what-is-a-namespace)
* [What is Kubernetes RBAC?](https://github.com/terraform-modules-krish/terraform-kubernetes-namespace/blob/main/modules/namespace-roles/README.md#what-is-kubernetes-role-based-access-control-rbac)
* [What is a Service Account?](https://github.com/terraform-modules-krish/terraform-kubernetes-namespace/blob/main/modules/service-account/README.md#what-is-a-serviceaccount)
* [Official Kubernetes Docs on Namespaces](https://kubernetes.io/docs/concepts/overview/working-with-objects/namespaces/)
* [Official Kubernetes Docs on Service Accounts](https://kubernetes.io/docs/reference/access-authn-authz/service-accounts-admin/)
* [Official Kubernetes Docs on RBAC](https://kubernetes.io/docs/reference/access-authn-authz/rbac/)

### Repo organization

* [modules](https://github.com/terraform-modules-krish/terraform-kubernetes-namespace/blob/main/modules): the main implementation code for this repo, broken down into multiple standalone, orthogonal submodules.
* [examples](https://github.com/terraform-modules-krish/terraform-kubernetes-namespace/blob/main/examples): This folder contains working examples of how to use the submodules.
* [test](https://github.com/terraform-modules-krish/terraform-kubernetes-namespace/blob/main/test): Automated tests for the modules and examples.




## Deploy

* [examples folder](https://github.com/terraform-modules-krish/terraform-kubernetes-namespace/blob/main/examples): The `examples` folder contains sample code optimized for learning, experimenting, and testing (but not production usage).



## Manage

* [How do you bind RBAC roles](https://github.com/terraform-modules-krish/terraform-kubernetes-namespace/blob/main/modules/namespace-roles/README.md#how-do-you-bind-the-roles)



## Support

If you need help with this repo or anything else related to infrastructure or DevOps, Gruntwork offers [Commercial Support](https://gruntwork.io/support/) via Slack, email, and phone/video. If you're already a Gruntwork customer, hop on Slack and ask away! If not, [subscribe now](https://www.gruntwork.io/pricing/). If you're not sure, feel free to email us at [support@gruntwork.io](mailto:support@gruntwork.io).




## Contributions

Contributions to this repo are very welcome and appreciated! If you find a bug or want to add a new feature or even contribute an entirely new module, we are very happy to accept pull requests, provide feedback, and run your changes through our automated test suite.

Please see [Contributing to the Gruntwork Infrastructure as Code Library](https://gruntwork.io/guides/foundations/how-to-use-gruntwork-infrastructure-as-code-library/#contributing-to-the-gruntwork-infrastructure-as-code-library) for instructions.




## License

Please see [LICENSE.txt](https://github.com/terraform-modules-krish/terraform-kubernetes-namespace/blob/main/LICENSE.txt) for details on how the code in this repo is licensed.
