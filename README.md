Kubernetes Cluster Monitoring on Zabbix.

Zabbix-Helm-Chart will create a zabbix-proxy POD while installtion.

root@rke2dscm1:~# kubectl get pod -n monitoring -o wide
NAME                                         READY   STATUS    RESTARTS         AGE   IP              NODE        NOMINATED NODE   READINESS GATES
zabbix-agent-ddql5                           1/1     Running   0                18h   10.10.10.5      rke2work1   <none>           <none>
zabbix-agent-m96xd                           1/1     Running   0                13d   10.10.10.7      rke2work2   <none>           <none>
zabbix-kube-state-metrics-64ddc65c45-g29d8   1/1     Running   1259 (10d ago)   13d   10.42.194.133   rke2work2   <none>           <none>
zabbix-proxy-78487cbbc4-qk8pg                1/1     Running   0                15h   10.42.194.140   rke2work2   <none>           <none>

Need to make changes for zabbix-proxy POD

Important files.

-rw-r----- 1 root root  417 Oct 24 19:14  zabbix-proxy-config.yaml
-rw-r----- 1 root root  960 Oct 24 19:25  zabbix-rbac.yaml
-rw-r----- 1 root root  993 Oct 24 19:29  zabbix-service-account.yaml
-rw-r----- 1 root root 3.2K Oct 24 19:31  zabbix-proxy-deployment.yaml

Optional :

-rw-r----- 1 root root 5.1K Oct 24 18:36  working-proxy.yaml
-rw-r----- 1 root root 1001 Oct 24 18:37  working-configmap.yaml

NOTE : All configuration steps yet to be added.
