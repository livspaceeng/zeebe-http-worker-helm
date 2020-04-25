# [zeebe-http-worker-helm](https://github.com/livspaceeng/zeebe-http-worker-helm)

Helm chart to host Zeebe Http worker app on Kubernetes cluster
> **Latest release: 0.5.0**

### Deployment Steps
- Clone these 2 repo in your home (**~**) directory:
  + [zeebe-http-worker-helm repo](https://github.com/livspaceeng/zeebe-http-worker-helm)
  + [helm-chart repo](https://github.com/livspaceeng/helm-charts)
- Make any required changes to [zeebe-http-worker-helm](https://github.com/livspaceeng/zeebe-http-worker-helm) repo.
- Update the **appVersion** in [Chart.yaml](./zeebe-http-worker/Chart.yaml) to point to the current [zeebe-http-worker version](https://github.com/livspaceeng/zeebe-http-worker/blob/master/pom.xml) (*Just to be aware of the current version being used*).
- Upgrade the **version** in [Chart.yaml](./zeebe-http-worker/Chart.yaml), and push to this repo.
- Run the below commands from terminal (*inside ~/helm-charts directory*):
  + `$ helm package ../zeebe-http-worker-helm/zeebe-http-worker`
  + `$ helm repo index --merge index.yaml --url https://charts.livspace.com .`
  + `$ git commit`
  + `$ git push origin`
- Use the **version** from [Chart.yaml](./zeebe-http-worker/Chart.yaml) and update it in [requirements.yaml](https://bitbucket.org/livspaceeng/environment-jx-dev/src/master/env/requirements.yaml).
