# openfaas-my-workshop
Test the openfaas on my workshop

## Work shop: 1

### Step 1: Install k3d to use kubernetes on macOS

#### Use homebrew to install k3d
```
$ brew install k3d
```
Check version
```
$ k3d --version
```
#### Usage

Check out what you can do via `k3d help`

Example Workflow: Create a new cluster and use it with `kubectl`
(*Note:* `kubectl` is not part of `k3d`, so you have to [install it first if needed](https://kubernetes.io/docs/tasks/tools/install-kubectl/))

1. `k3d create` to create a new single-node cluster (docker container)
2. `export KUBECONFIG=$(k3d get-kubeconfig)` to make `kubectl` to use the kubeconfig for that cluster
3. execute some commands like `kubectl get pods --all-namespaces`
4. `k3d delete` to delete the default cluster
