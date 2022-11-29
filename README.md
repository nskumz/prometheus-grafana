we will install and setup these tools through helm chart.

so,we will use **kube-prometheus-stack** helm chart in this helm charts we will have all the latest components for prometheus & grafana.

so in command line search like ---> helm search repo | grep kube-prometheus-stack

you can find the helm chart and install it in local

you can find these like below 




NAME                                                               READY   STATUS    RESTARTS        AGE

pod/alertmanager-monitoring-cm-kube-prometh-alertmanager-0         2/2     Running   3 (3h27m ago)   23h

pod/monitoring-cm-grafana-758f468468-ncd8t                         3/3     Running   3 (3h27m ago)   23h

pod/monitoring-cm-kube-prometh-operator-864c99b4cd-87rss           1/1     Running   1 (3h27m ago)   23h

pod/monitoring-cm-kube-state-metrics-6c94544dcb-qvvxk              1/1     Running   3 (3h21m ago)   23h

pod/monitoring-cm-prometheus-node-exporter-jlb95                   1/1     Running   1 (3h27m ago)   23h

pod/prometheus-monitoring-cm-kube-prometh-prometheus-0             2/2     Running   2 (3h27m ago)   23h


NAME                                              TYPE        CLUSTER-IP      EXTERNAL-IP   PORT(S)                      AGE
service/alertmanager-operated                     ClusterIP   None            <none>        9093/TCP,9094/TCP,9094/UDP   23h
service/monitoring-cm-grafana                     ClusterIP   10.96.244.224   <none>        80/TCP                       23h
service/monitoring-cm-kube-prometh-alertmanager   ClusterIP   10.96.90.239    <none>        9093/TCP                     23h
service/monitoring-cm-kube-prometh-operator       ClusterIP   10.96.32.22     <none>        443/TCP                      23h
service/monitoring-cm-kube-prometh-prometheus     ClusterIP   10.96.230.8     <none>        9090/TCP                     23h
service/monitoring-cm-kube-state-metrics          ClusterIP   10.96.142.162   <none>        8080/TCP                     23h
service/monitoring-cm-prometheus-node-exporter    ClusterIP   10.96.240.211   <none>        9100/TCP                     23h
service/prometheus-operated                       ClusterIP   None            <none>        9090/TCP                     23h

NAME                                                    DESIRED   CURRENT   READY   UP-TO-DATE   AVAILABLE   NODE SELECTOR   AGE
daemonset.apps/monitoring-cm-prometheus-node-exporter   1         1         1       1            1           <none>          23h

NAME                                                  READY   UP-TO-DATE   AVAILABLE   AGE
deployment.apps/monitoring-cm-grafana                 1/1     1            1           23h
deployment.apps/monitoring-cm-kube-prometh-operator   1/1     1            1           23h
deployment.apps/monitoring-cm-kube-state-metrics      1/1     1            1           23h

NAME                                                             DESIRED   CURRENT   READY   AGE
replicaset.apps/monitoring-cm-grafana-758f468468                 1         1         1       23h
replicaset.apps/monitoring-cm-kube-prometh-operator-864c99b4cd   1         1         1       23h
replicaset.apps/monitoring-cm-kube-state-metrics-6c94544dcb      1         1         1       23h

NAME                                                                    READY   AGE
statefulset.apps/alertmanager-monitoring-cm-kube-prometh-alertmanager   1/1     23h
statefulset.apps/prometheus-monitoring-cm-kube-prometh-prometheus       1/1     23h

so to access the prometheus and grafana use kubectl port-forward with respected port numbers.
