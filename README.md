# tekton-example

## Installing Tekton Pipelines on Kubernetes

To [install](https://github.com/tektoncd/pipeline/blob/master/docs/install.md#installing-tekton-pipelines-on-kubernetes) Tekton Pipelines on a Kubernetes cluster:

Run the following command to install Tekton Pipelines and its dependencies:

```
kubectl apply --filename https://storage.googleapis.com/tekton-releases/pipeline/latest/release.yaml
```

## Tekton Dashboard

### Using [kubectl port-forward](https://github.com/tektoncd/dashboard/blob/master/docs/install.md#using-kubectl-port-forward)

Assuming tekton-pipelines is the install namespace for the Dashboard, run the following command:

```
kubectl --namespace tekton-pipelines port-forward svc/tekton-dashboard 9097:9097
```

Browse http://localhost:9097 to access your Dashboard.

### Uninstalling the Dashboard on Kubernetes

The Dashboard can be [uninstalled](https://github.com/tektoncd/dashboard/blob/master/docs/install.md) by running the following command:

```
kubectl delete --filename https://storage.googleapis.com/tekton-releases/dashboard/latest/tekton-dashboard-release.yaml
```

The above command assumes that the latest version was installed, refer to Installing Tekton Dashboard on Kubernetes to find the correct --filename argument if another version was installed.
