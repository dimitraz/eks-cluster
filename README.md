# Provisioning an EKS Cluster

Provisioning an EKS cluster for my final year project.

### Running pods

```
NAMESPACE     NAME                                           READY   STATUS             RESTARTS   AGE
default       nginx-deployment-6fdbb596db-zfk6c              1/1     Running            0          41m
demo          kafka-consumer-f4cff8b79-v52mj                 1/1     Running            4          4m
demo          kafka-producer-5c77885465-fqgh6                1/1     Running            0          2m
kafka         my-cluster-entity-operator-584f777568-rvxsn    3/3     Running            0          8m
kafka         my-cluster-kafka-0                             2/2     Running            0          9m
kafka         my-cluster-kafka-1                             2/2     Running            0          9m
kafka         my-cluster-kafka-2                             2/2     Running            0          9m
kafka         my-cluster-zookeeper-0                         2/2     Running            0          10m
kafka         my-cluster-zookeeper-1                         2/2     Running            0          10m
kafka         my-cluster-zookeeper-2                         2/2     Running            0          10m
kafka         strimzi-cluster-operator-c8d786dcb-jjp79       1/1     Running            0          10m
kube-system   aws-node-2nf5q                                 1/1     Running            0          44m
kube-system   aws-node-4lwr8                                 1/1     Running            0          43m
kube-system   aws-node-8ndrt                                 1/1     Running            0          43m
kube-system   coredns-7554568866-lk94m                       1/1     Running            0          55m
kube-system   coredns-7554568866-zlg67                       1/1     Running            0          55m
kube-system   heapster-84c9bc48c4-qwrg9                      1/1     Running            0          15m
kube-system   kube-proxy-8pkhk                               1/1     Running            0          43m
kube-system   kube-proxy-ft5h5                               1/1     Running            0          44m
kube-system   kube-proxy-xhghc                               1/1     Running            0          43m
kube-system   kubernetes-dashboard-5dd89b9875-5swmq          1/1     Running            0          16m
kube-system   monitoring-influxdb-848b9b66f6-2r5ln           1/1     Running            0          15m
kubeless      kubeless-controller-manager-76b5c84b88-sj97h   3/3     Running            0          6m
```

### Deployments

```
NAMESPACE     NAME                          DESIRED   CURRENT   UP-TO-DATE   AVAILABLE   AGE
demo          kafka-consumer                1         1         1            0           6m
demo          kafka-producer                1         1         1            1           6m
kafka         my-cluster-entity-operator    1         1         1            1           10m
kafka         strimzi-cluster-operator      1         1         1            1           12m
kube-system   coredns                       2         2         2            2           57m
kube-system   heapster                      1         1         1            1           17m
kube-system   kubernetes-dashboard          1         1         1            1           17m
kube-system   monitoring-influxdb           1         1         1            1           17m
kubeless      kubeless-controller-manager   1         1         1            1           7m
```
