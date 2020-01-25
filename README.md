## A Sample Kubernetes Operator
---
A Kubernetes operator is a high-level description of a deployable application to be run in a Kubernetes cluster. This is a tiny Kubernetes operator written with **KUDO** (Kubernetes Universal Declarative Operator) to set default cpu and memory limits on every deployment and statefulset that doesn't have them.

### How to Run
---

- Clone the repo to your system by `git clone https://github.com/kishorgec/kudo-operator.git`

- Make sure that you have the latest kubectl and kudo plugin installed. If not, please follow the instructions here : https://kudo.dev/docs/#pre-requisites

- Open terminal and type commands to install and makes a working operator instance running in your Kubernetes cluster. The operator will be created in your default namespace unless you provide an explicit namespace argument.

```
kubectl kudo install kudo-operator/

kubectl kudo plan status --instance my-kudo-operator-instance

kubectl kudo update --instance my-kudo-operator-instance -p MEMORY=180Mi

kubectl kudo upgrade ../kudo-operator/ --instance my-kudo-operator-instance

kubectl kudo uninstall --instance my-kudo-operator-instance

kubectl delete operator my-kudo-operator

```

### Future
---

- If you need to use this operator for your custom services that you are developing, add your preformatted service YAML to the template folder and then follow the instructions above. Ignore the sample nginx services if needed.

### Resources
---
  - [Kudo Operator](https://kudo.dev/docs/#create-your-first-operator)
  - [Kudo Architecture](https://kudo.dev/docs/architecture.html#architecture-diagram)
  - [LimitRanges Kubernetes](https://kubernetes.io/docs/concepts/policy/limit-range/)