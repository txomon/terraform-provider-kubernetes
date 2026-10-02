<a href="https://terraform.io">
    <img src=".github/tf.png" alt="Terraform logo" title="Terraform" align="left" height="50" />
</a>

# Patched Kubernetes Provider for Terraform [![GitHub tag (latest SemVer)](https://img.shields.io/github/v/tag/hashicorp/terraform-provider-kubernetes?label=release)](https://github.com/hashicorp/terraform-provider-kubernetes/releases) [![license](https://img.shields.io/github/license/hashicorp/terraform-provider-kubernetes.svg)]()

This provider is a patched one when compared to the official terraform provider.

All the patches can be found separately in branches:

* `fix-strict-lists` Fixes errors raised for incompatible Tuples `AttributeName("name"): can't use tftypes.Tuple[...] as tftypes.Tuple[...]` because of subitems having object attributes with no fields but annotated with `x-kubernetes-preserve-unknown-fields`, https://github.com/txomon/terraform-provider-kubernetes/issues/1

Patches no longer carried because upstream fixed them:

* `fix-replacement` Supressed forced replacement on attributes annotated with `x-kubernetes-preserve-unknown-fields`, https://github.com/hashicorp/terraform-provider-kubernetes/issues/1893. Fixed upstream in v2.33.0 by https://github.com/hashicorp/terraform-provider-kubernetes/pull/2437


Other branches:
* `main` branch follows [upstream main](https://github.com/hashicorp/terraform-provider-kubernetes)
* `master` has upstream merged with the different branches to enable parallel releases https://registry.terraform.io/providers/txomon/kubernetes
