# Voting_app_observation_subhadip_13.228.21.240

Last login: Tue Oct 29 04:39:03 2024 from 103.219.45.157
ubuntu@ip-172-31-34-217:~$ sudo -i
root@ip-172-31-34-217:~#
root@ip-172-31-34-217:~#
root@ip-172-31-34-217:~# cd /root/
root@ip-172-31-34-217:~#
root@ip-172-31-34-217:~# git clone https://github.com/ashishrpandey/example-voting-app
fatal: destination path 'example-voting-app' already exists and is not an empty directory.
root@ip-172-31-34-217:~# cd /root/example-voting-app/k8s-specifications
root@ip-172-31-34-217:~/example-voting-app/k8s-specifications#
root@ip-172-31-34-217:~/example-voting-app/k8s-specifications#
root@ip-172-31-34-217:~/example-voting-app/k8s-specifications# kubectl apply -f
error: flag needs an argument: 'f' in -f
See 'kubectl apply --help' for usage.
root@ip-172-31-34-217:~/example-voting-app/k8s-specifications# kubectl apply -f .
deployment.apps/db created
service/db created
deployment.apps/redis created
service/redis created
deployment.apps/result created
service/result created
deployment.apps/vote created
service/vote created
deployment.apps/worker created
root@ip-172-31-34-217:~/example-voting-app/k8s-specifications# ipconfig
Command 'ipconfig' not found, did you mean:
  command 'ifconfig' from deb net-tools (1.60+git20181103.0eebece-1ubuntu5)
  command 'iwconfig' from deb wireless-tools (30~pre9-13.1ubuntu4)
  command 'iconfig' from deb ipmiutil (3.1.8-1)
Try: apt install <deb name>
root@ip-172-31-34-217:~/example-voting-app/k8s-specifications# ifconfig
Command 'ifconfig' not found, but can be installed with:
apt install net-tools
root@ip-172-31-34-217:~/example-voting-app/k8s-specifications# kubectl get po -o wide
NAME                             READY   STATUS    RESTARTS   AGE     IP              NODE               NOMINATED NODE   READINESS GATES
db-58cc845644-278k4              1/1     Running   0          3m23s   192.168.16.85   ip-172-31-34-217   <none>           <none>
mavenir-mysql-5bd9db6849-5rwkf   0/1     Pending   0          24h     <none>          <none>             <none>           <none>
redis-6878558678-b2s8j           1/1     Running   0          3m23s   192.168.16.86   ip-172-31-34-217   <none>           <none>
result-86bc6f7b5d-qdfr7          1/1     Running   0          3m23s   192.168.16.87   ip-172-31-34-217   <none>           <none>
vote-7d884dd585-c7z45            1/1     Running   0          3m23s   192.168.16.88   ip-172-31-34-217   <none>           <none>
worker-6fc5d5b668-6c55n          1/1     Running   0          3m23s   192.168.16.89   ip-172-31-34-217   <none>           <none>
root@ip-172-31-34-217:~/example-voting-app/k8s-specifications# kubectl get po, svc -o wide
error: arguments in resource/name form must have a single resource and name
root@ip-172-31-34-217:~/example-voting-app/k8s-specifications# kubectl get svc -o wide
NAME            TYPE        CLUSTER-IP       EXTERNAL-IP   PORT(S)          AGE     SELECTOR
db              ClusterIP   10.107.29.178    <none>        5432/TCP         3m59s   app=db
kubernetes      ClusterIP   10.96.0.1        <none>        443/TCP          25h     <none>
mavenir-mysql   ClusterIP   10.106.152.129   <none>        3306/TCP         24h     app=mavenir-mysql
redis           ClusterIP   10.105.239.175   <none>        6379/TCP         3m59s   app=redis
result          NodePort    10.99.172.224    <none>        5001:31003/TCP   3m59s   app=result
vote            NodePort    10.104.22.196    <none>        5000:31002/TCP   3m59s   app=vote
root@ip-172-31-34-217:~/example-voting-app/k8s-specifications#

 /root/example-voting-app/result
-bash: /root/example-voting-app/result: Is a directory
root@ip-172-31-34-217:~/example-voting-app/k8s-specifications# cd /root/example-voting-app/result/
root@ip-172-31-34-217:~/example-voting-app/result# ls
Dockerfile  docker-compose.test.yml  package.json  server.js  tests  views
root@ip-172-31-34-217:~/example-voting-app/result# vi server.js
root@ip-172-31-34-217:~/example-voting-app/result#
