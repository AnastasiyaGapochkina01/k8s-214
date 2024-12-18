```
~/214-k8s$ kubectl apply -f nginx-214.yml
~/214-k8s$ kubectl get pod
NAME               READY   STATUS                   RESTARTS   AGE
214-nginx          1/1     Running                  0          8h
app-rs-cff5j       1/1     Running                  1          4d11h
app-rs-gcpkz       1/1     Running                  1          4d11h
app-rs-jbk2n       1/1     Running                  1          4d11h
app-rs-tsnxx       1/1     Running                  1          4d11h
main-nginx         1/1     Running                  2          4d12h
manifested-nginx   1/1     Running                  2          4d12h
nginx-214          1/1     Running                  0          3m5s
node-app           1/1     Running                  0          8h
sidecar-nginx      2/2     Running                  4          4d12h
test-nginx         0/1     ContainerStatusUnknown   1          4d12h
~/214-k8s$ kubectl get svc
NAME            TYPE        CLUSTER-IP       EXTERNAL-IP   PORT(S)        AGE
kubernetes      ClusterIP   10.96.0.1        <none>        443/TCP        4d13h
nginx-svc       ClusterIP   10.100.84.79     <none>        80/TCP         4d12h
nginx-svc-214   NodePort    10.103.156.222   <none>        80:32457/TCP   3m56s
node-app-svc    ClusterIP   10.105.52.8      <none>        8080/TCP       8h

curl <vm-ip>:32457
```
