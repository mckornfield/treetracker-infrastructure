### Authenticating to kubernetes clusters

1. Install doctl, `brew install doctl` on mac
2. Use `doctl auth init` and pass your DO API key
3. Save the kubeconfig relevant to the cluster, e.g. `doctl kubernetes cluster kubeconfig save dev-k8s-treetracker`
4. Switch to the context if not already switched, e.g. `kubectl config set-context do-sfo2-dev-k8s-treetracker` You can view the relevant contexts using `kubectl config view | grep treetracker`
2-4 can be done using `./scripts/doctl_setup.sh CLUSTER_NAME`, e.g. `./scripts/doctl_setup.sh dev-k8s-treetracker`
5. Install helm 3 if not present, `brew install helm`
6. You are now ready to run any helm command/ playbooks relevant to the repo

### Cluster names
* dev-k8s-treetracker
* test-k8s-treetracker
