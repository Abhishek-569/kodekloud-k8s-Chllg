## Martin
To create a Martin User in Kubeconfig:
```
kubectl config set-credentials martin --client-certificate=/root/martin.crt --client-key=/root/martin.key --kubeconfig=$HOME/.kube/config
```
This command adds a new user named martin to the default kubeconfig file ($HOME/.kube/config) with the specified client-certificate and client-key paths.
```
kubectl config set-context developer --user=martin --cluster=kubernetes --kubeconfig=$HOME/.kube/config
```
This command creates a new context named developer in the default kubeconfig file ($HOME/.kube/config) with the specified user (martin) and cluster (kubernetes) settings.


## Kube-config
You can set the developer context with user martin and cluster kubernetes as the current context using the kubectl config use-context command, like this:
```
kubectl config use-context developer --user=martin --cluster=kubernetes
```
This command sets the developer context, and specifies the --user flag with value martin and the --cluster flag with value kubernetes to associate the context with the desired user and cluster. Once this command is executed, the developer context will be set as the current context in the kubeconfig file, and future kubectl commands will use it by default.
