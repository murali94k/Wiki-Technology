## kubectl Basic Commands

| Commands                                                   | Description                                                                          |
|------------------------------------------------------------|--------------------------------------------------------------------------------------|
| `kubectl get pods` | Show all pods status|
| `kubectl get deployment` | Show all deployments |
| `kubectl get all` | |
| `kubectl describe pod <name>` | Show details of the component (pod) specified |
| `kubectl create -f Deployment.yaml` | Create new deployment |
| `kubectl apply -f Deploymant.yaml` | Apply changes to existing deployment|
| `kubectl delete deployment <name>` | Removes the deployment|

## Minikube commands

| Commands                                                   | Description                                                                          |
|------------------------------------------------------------|--------------------------------------------------------------------------------------|
|`minikube dashboard` | Show kubernetes dashboard in browser |
|`minikube service <service_name> --url` | Get url for accessing the pods within the service|
|`minikube get nodes` | get the names of all the nodes|
|`minikube ssh -n <node>` | SSH into the node | 


## Helm commands

| Commands                                                   | Description                                                                          |
|------------------------------------------------------------|--------------------------------------------------------------------------------------|
| `helm create <helm-chart-name>`  | Creates all the yaml files to build helm chart|
| `helm template <chart-dir-path> [<repo-name>]` | Spits out the yaml for the helm after processing files in templates folder in the path |
| `helm install <release-name> <chart-dir-path> [<repo-name>]` | Process all the templates and deploy the yaml |
