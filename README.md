# Telemetry Platform on Kubernetes with Canary Releases and Chaos Tests

**Status: in progress.** This repository is being built; nothing here is a finished result yet.

## Goal

The platform for the telemetry pipeline: EKS and networking provisioned with Terraform, GitHub Actions CI and Argo CD GitOps, canary releases gated on Prometheus SLOs with automatic rollback, an Istio mesh with mTLS, OpenTelemetry tracing into Grafana, and Chaos Mesh experiments under load.

## Layout

```
terraform/modules/vpc/    # VPC module.
terraform/modules/eks/    # EKS module.
terraform/envs/dev/       # Dev environment.
k8s/base/                 # Base manifests.
k8s/overlays/dev/         # Dev overlay.
argocd/                   # Argo CD Application manifests.
rollouts/                 # Canary strategy and SLO analysis templates.
istio/                    # Mesh config and mTLS policy.
observability/            # Prometheus rules, Grafana dashboards, OpenTelemetry collector.
chaos/                    # Chaos Mesh experiments.
ci/                       # CI notes; workflows go in .github/workflows/
docs/                     # Runbook, cost notes (tear down daily) and results.
```

## Plan

- [ ] Terraform VPC + EKS
- [ ] CI (GitHub Actions)
- [ ] Argo CD GitOps
- [ ] Canary + SLO analysis + rollback
- [ ] Istio mTLS
- [ ] OpenTelemetry tracing + Grafana
- [ ] Chaos Mesh experiments
- [ ] Write-up
