# Info

Some k8s manifests I used for my needs 

- Deployed Kubernetes with _k0sctl_
- _MetalLB_ for exposing services through IPs
- _Traefik_ for ingress and tls
- _Jenkins_ for CI/CD
- _SonarQube_ for code analysis
- _local-path-provisioner_ for easy storage managing
- _prometheus-stack_ for monitoring

## Bare-metal Kubernetes for working

1. Install k8s using k0s, see [guide](k0sctl/README.md)
2. Create local path provisioner, see [guide](local-path-provisioner/README.md)
3. Install MetalLB, see [guide](metallb/README.md)
4. Install Traefik, see [guide](traefik/README.md)
5. Start monitoring, see [guide](prometheus-stack/README.md)
 