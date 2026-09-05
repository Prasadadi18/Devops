minikube start
😄  minikube v1.38.1 on Microsoft Windows 11 Home Single Language 25H2
✨  Using the docker driver based on existing profile
👍  Starting "minikube" primary control-plane node in "minikube" cluster
🚜  Pulling base image v0.0.50 ...
🔄  Restarting existing docker container for "minikube" ... 
🐳  Preparing Kubernetes v1.35.1 on Docker 29.2.1 ... 
🔎  Verifying Kubernetes components...
    ▪ Using image gcr.io/k8s-minikube/storage-provisioner:v5
🌟  Enabled addons: storage-provisioner, default-storageclass
🏄  Done! kubectl is now configured to use "minikube" cluster and "default" namespace by default
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment2> minikube docker-env
$Env:DOCKER_TLS_VERIFY = "1"
$Env:DOCKER_HOST = "tcp://127.0.0.1:60859"
$Env:DOCKER_CERT_PATH = "C:\Users\adina\.minikube\certs"
$Env:MINIKUBE_ACTIVE_DOCKERD = "minikube"
# To point your shell to minikube's docker-daemon, run:
# & minikube -p minikube docker-env --shell powershell | Invoke-Expression

(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment2> & minikube -p minikube docker-env --shell powershell | Invoke-Expression
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment2> pip install flask
Requirement already satisfied: flask in c:\users\adina\anaconda3\lib\site-packages (3.0.0)
Requirement already satisfied: Werkzeug>=3.0.0 in c:\users\adina\anaconda3\lib\site-packages (from flask) (3.0.3)
Requirement already satisfied: Jinja2>=3.1.2 in c:\users\adina\anaconda3\lib\site-packages (from flask) (3.1.4)
Requirement already satisfied: itsdangerous>=2.1.2 in c:\users\adina\anaconda3\lib\site-packages (from flask) (2.2.0)
Requirement already satisfied: click>=8.1.3 in c:\users\adina\anaconda3\lib\site-packages (from flask) (8.3.3)
Requirement already satisfied: blinker>=1.6.2 in c:\users\adina\anaconda3\lib\site-packages (from flask) (1.6.2)
Requirement already satisfied: colorama in c:\users\adina\anaconda3\lib\site-packages (from click>=8.1.3->flask) (0.4.6)
Requirement already satisfied: MarkupSafe>=2.0 in c:\users\adina\anaconda3\lib\site-packages (from Jinja2>=3.1.2->flask) (2.1.3)
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment2> docker build -t flask-app .
[+] Building 47.4s (9/9) FINISHED                                                                                                                             docker:default
 => [internal] load build definition from Dockerfile                                                                                                                    0.2s
 => => transferring dockerfile: 133B                                                                                                                                    0.1s
 => [internal] load metadata for docker.io/library/python:3.8-slim                                                                                                      2.9s
 => [internal] load .dockerignore                                                                                                                                       0.1s
 => => transferring context: 2B                                                                                                                                         0.0s
 => [internal] load build context                                                                                                                                       0.1s
 => => transferring context: 13.13kB                                                                                                                                    0.0s
 => [1/4] FROM docker.io/library/python:3.8-slim@sha256:1d52838af602b4b5a831beb13a0e4d073280665ea7be7f69ce2382f29c5a613f                                               25.8s
 => => resolve docker.io/library/python:3.8-slim@sha256:1d52838af602b4b5a831beb13a0e4d073280665ea7be7f69ce2382f29c5a613f                                                0.0s
 => => sha256:1d52838af602b4b5a831beb13a0e4d073280665ea7be7f69ce2382f29c5a613f 10.41kB / 10.41kB                                                                        0.0s
 => => sha256:314bc2fb0714b7807bf5699c98f0c73817e579799f2d91567ab7e9510f5601a5 1.75kB / 1.75kB                                                                          0.0s
 => => sha256:b5f62925bd0f63f48cc8acd5e87d0c3a07e2f229cd2fb0a9586e68ed17f45ee3 5.25kB / 5.25kB                                                                          0.0s
 => => sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab 29.13MB / 29.13MB                                                                        6.7s
 => => sha256:030d7bdc20a63e3d22192b292d006a69fa3333949f536d62865d1bd0506685cc 3.51MB / 3.51MB                                                                          1.7s
 => => sha256:a3f1dfe736c5f959143f23d75ab522a60be2da902efac236f4fb2a153cc14a5d 14.53MB / 14.53MB                                                                        4.8s
 => => sha256:3971691a363796c39467aae4cdce6ef773273fe6bfc67154d01e1b589befb912 248B / 248B                                                                              2.1s
 => => extracting sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab                                                                              10.8s
 => => extracting sha256:030d7bdc20a63e3d22192b292d006a69fa3333949f536d62865d1bd0506685cc                                                                               1.3s
 => => extracting sha256:a3f1dfe736c5f959143f23d75ab522a60be2da902efac236f4fb2a153cc14a5d                                                                               5.6s
 => => extracting sha256:3971691a363796c39467aae4cdce6ef773273fe6bfc67154d01e1b589befb912                                                                               0.0s
 => [2/4] WORKDIR /app                                                                                                                                                  0.3s
 => [3/4] COPY . /app                                                                                                                                                   0.1s
 => [4/4] RUN pip install flask                                                                                                                                        16.4s
 => exporting to image                                                                                                                                                  1.0s
 => => exporting layers                                                                                                                                                 0.9s
 => => writing image sha256:7ce91aab7008a02bd7fb35c546b0e8a2e285cfdfa9c35f8a1c9906f36f10327e                                                                            0.0s
 => => naming to docker.io/library/flask-app                                                                                                                            0.0s

View build details: docker-desktop://dashboard/build/default/default/mzb27d2tgc8jl539afut1dili
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment2> kubectl apply -f flask-deployment.yaml
error: the path "flask-deployment.yaml" does not exist
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment2> kubectl apply -f flask-deployment.yaml
deployment.apps/flask-app created
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment2> kubectl get deployments
NAME        READY   UP-TO-DATE   AVAILABLE   AGE
flask-app   1/1     1            1           11s
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment2> kubectl get pods -l app=flask-app
NAME                         READY   STATUS    RESTARTS   AGE
flask-app-6d58f88547-98rnf   1/1     Running   0          21s
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment2> kubectl describe deployment flask-app
Name:                   flask-app
Namespace:              default
CreationTimestamp:      Sun, 30 Aug 2026 12:15:43 +0530
Labels:                 <none>
Annotations:            deployment.kubernetes.io/revision: 1
Selector:               app=flask-app
Replicas:               1 desired | 1 updated | 1 total | 1 available | 0 unavailable
StrategyType:           RollingUpdate
MinReadySeconds:        0
RollingUpdateStrategy:  25% max unavailable, 25% max surge
Pod Template:
  Labels:  app=flask-app
  Containers:
   flask-app:
    Image:         flask-app:latest
    Port:          15000/TCP
    Host Port:     0/TCP
    Environment:   <none>
    Mounts:        <none>
  Volumes:         <none>
  Node-Selectors:  <none>
  Tolerations:     <none>
Conditions:
  Type           Status  Reason
  ----           ------  ------
  Available      True    MinimumReplicasAvailable
  Progressing    True    NewReplicaSetAvailable
OldReplicaSets:  <none>
NewReplicaSet:   flask-app-6d58f88547 (1/1 replicas created)
Events:
  Type    Reason             Age   From                   Message
  ----    ------             ----  ----                   -------
  Normal  ScalingReplicaSet  34s   deployment-controller  Scaled up replica set flask-app-6d58f88547 from 0 to 1
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment2> kubectl logs flask-app-6d58f88547-98rnf
 * Serving Flask app 'app'
 * Debug mode: off
WARNING: This is a development server. Do not use it in a production deployment. Use a production WSGI server instead.
 * Running on all addresses (0.0.0.0)
 * Running on http://127.0.0.1:15000
 * Running on http://10.244.0.8:15000
Press CTRL+C to quit
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment2> kubectl get services
NAME         TYPE        CLUSTER-IP       EXTERNAL-IP   PORT(S)        AGE
hello-k8s    NodePort    10.106.156.184   <none>        80:30346/TCP   15h
kubernetes   ClusterIP   10.96.0.1        <none>        443/TCP        15h
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment2> curl  http://127.0.0.1:15000
curl : Unable to connect to the remote server
At line:1 char:1
+ curl  http://127.0.0.1:15000
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : InvalidOperation: (System.Net.HttpWebRequest:HttpWebRequest) [Invoke-WebRequest], WebException
    + FullyQualifiedErrorId : WebCmdletWebResponseException,Microsoft.PowerShell.Commands.InvokeWebRequestCommand
 
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment2> kubectl apply -f flask-deployment.yaml
service/flask-app-service created
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment2> minikube service flask-app-service --url
http://127.0.0.1:59850
❗  Because you are using a Docker driver on windows, the terminal needs to be open to run it.
