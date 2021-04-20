# Nexus3 Repository Helm Chart
This Helm Chart was written to quick deploy Nexus3 Repository to Kubernetes
## What will this chart do?
#### This chart will deploy Nexus3 Repository to your K8s Cluster
- On Kubernetes Side:
1. Apply Deployment
2. Apply Service for UI
3. Apply Services for Repositories
4. Create/Apply SSL Certificates
5. Apply Ingress with SSL
6. Create PVC for Deployment(Heketi)

## How to run ?
1. First of all edit the `values.yaml` file
2. Execute the *Helm*

To run just execute the command like below:
```bash
helm upgrade --install -f values.yaml nexus-oss . --namespace my-namespace
```
