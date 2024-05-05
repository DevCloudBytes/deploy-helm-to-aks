
# helm-demo1

- cd `helm-demo1`
- `helm package .`
- helm installation `helm install mywebapp ./mywebapp-0.1.0.tgz`
```text
NAME: mywebapp
LAST DEPLOYED: Sun May  5 14:25:34 2024
NAMESPACE: default
STATUS: deployed
REVISION: 1
TEST SUITE: None
```
- `helm list`
```text
NAME            NAMESPACE       REVISION        UPDATED                                 STATUS          CHART           APP VERSION
mywebapp        default         1               2024-05-05 14:25:34.9424614 -0400 EDT   deployed        mywebapp-0.1.0
```

- `kubectl get all`
```text
  NAME                            READY   STATUS    RESTARTS   AGE
  pod/mywebapp-746876f576-2qs6t   1/1     Running   0          9m43s
  pod/mywebapp-746876f576-lj4zg   1/1     Running   0          9m43s

NAME                 TYPE        CLUSTER-IP   EXTERNAL-IP   PORT(S)   AGE
service/kubernetes   ClusterIP   10.0.0.1     <none>        443/TCP   69m

NAME                       READY   UP-TO-DATE   AVAILABLE   AGE
deployment.apps/mywebapp   2/2     2            2           9m44s

NAME                                  DESIRED   CURRENT   READY   AGE
replicaset.apps/mywebapp-746876f576   2         2         2       9m43s
```
 