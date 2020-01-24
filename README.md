## My First Kubernetes Operator

A Kubernetes operator is a high-level description of a deployable application to be run in a Kubernetes cluster. This is a sample Kubernetes operator written with **KUDO** (Kubernetes Universal Declarative Operator). 

### How to Run

- Clone the repo to your system by `git clone https://github.com/kishorgec/kudo-operator.git`

- Make sure that you have the latest kubectl and kudo plugin installed. If not please follow the instructions here : https://kudo.dev/docs/#pre-requisites

- Open terminal and type commands to install and makes a working operator instance running in your Kubernetes cluster. The operator will be created in your default namespace unless you provide an explicit namespace argument.

```
kubectl kudo install kudo-operator/

kubectl kudo plan status --instance my-kudo-operator-instance

kubectl kudo update --instance my-kudo-operator-instance -p replicas=2

kubectl kudo upgrade ../kudo-operator/  --instance my-kudo-operator-instance

kubectl kudo uninstall --instance my-kudo-operator-instance

kubectl delete operator my-kudo-operator
```
