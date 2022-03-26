# Install the CRD on the kubernetes server

`kubectl create namespace argo-rollouts`{{execute}}
`kubectl apply -n argo-rollouts -f https://github.com/argoproj/argo-rollouts/releases/latest/download/install.yaml`{{execute}}


You can check if the installation is succesful by using the following query : 
`kubectl get XXXXXX` # TODO

# Install the plugin on the local client

```bash
curl -LO https://github.com/argoproj/argo-rollouts/releases/latest/download/kubectl-argo-rollouts-linux-amd64
chmod +x ./kubectl-argo-rollouts-darwin-amd64
sudo mv ./kubectl-argo-rollouts-darwin-amd64 /usr/local/bin/kubectl-argo-rollouts
```{{execute}}

You should now be able to use the argo rollouts plugin : 

`kubectl argo rollouts version`{{execute}}