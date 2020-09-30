# Redis Server via Helm3

Simple chart to create Redis Server under your namespace
For example you have a `CoolApp` under "CoolApp" namespace within K8S components (Deployment,Service,Ingress and etc.)
and you need to add Redis Server here

- To Install or Upgrade just execute the command below:
```bash
$ helm upgrade --install --force redis . -f values.yaml --set ns_name=CoolApp,ms_names.name=redis,image.version=latest --namespace CoolApp
```
- To delete it:
```
$ helm delete redis -n CoolApp
```
- And finally you can get Cluster IP and Port from the Redis Service:
```bash
$ kubectl -n CoolApp get svc
```