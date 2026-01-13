# helm-kyverno

A Crossplane Configuration package that installs the Kyverno Helm chart with a minimal, stable interface.

## Overview

`helm-kyverno` renders a single Helm release for Kyverno. It exposes only the inputs needed
for chart values, namespace, and release name, keeping the interface stable while allowing full Helm overrides.

## Features

- **Minimal Helm interface**: values and overrideAllValues with stable defaults
- **Predictable naming**: defaults to `<clusterName>-kyverno` in the `kyverno` namespace
- **GitOps friendly**: ships a `.gitops/` deploy chart

## Prerequisites

- Crossplane installed in the cluster
- Crossplane providers:
  - `provider-helm` (>=v1.0.2)
- Crossplane function:
  - `function-auto-ready` (>=v0.6.0)

## Quick Start

```yaml
apiVersion: pkg.crossplane.io/v1
kind: Configuration
metadata:
  name: helm-kyverno
spec:
  package: ghcr.io/hops-ops/helm-kyverno:latest
```

```yaml
apiVersion: helm.hops.ops.com.ai/v1alpha1
kind: Kyverno
metadata:
  name: kyverno
  namespace: example-env
spec:
  clusterName: example-cluster
  values:
    admissionController:
      replicas: 3
```

## Development

```bash
make render
make validate
make test
```
