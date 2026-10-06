(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops> cd Assignment3                             
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment3> docker build -t adi18prasad/flashsale:1.0 .
[+] Building 85.2s (10/10) FINISHED                                                                                               docker:desktop-linux
 => [internal] load build definition from Dockerfile                                                                                              0.1s
 => => transferring dockerfile: 227B                                                                                                              0.0s
 => [internal] load metadata for docker.io/library/python:3.11-slim                                                                               1.6s
 => [auth] library/python:pull token for registry-1.docker.io                                                                                     0.0s
 => [internal] load .dockerignore                                                                                                                 0.0s
 => => transferring context: 2B                                                                                                                   0.0s
 => [1/4] FROM docker.io/library/python:3.11-slim@sha256:9534e5a8e315485d4061ed659af0fd78a284c015f9b73661b41d6bab25604534                        17.3s
 => => resolve docker.io/library/python:3.11-slim@sha256:9534e5a8e315485d4061ed659af0fd78a284c015f9b73661b41d6bab25604534                         0.1s
 => => sha256:3678bb828654fcc3752f7a5eb63c5accfa00c97047252f25405285550d74a3fd 4.27MB / 4.27MB                                                    2.3s
 => => sha256:6310eb16bf4251731feab01e8f633bf5e2d75a657ccad97f420b1f83cce457be 29.79MB / 29.79MB                                                  7.7s
 => => sha256:f9efa1b83d065a7c5a3041582875b75d63c4ab3d4413514de8e413b51f90e91a 249B / 249B                                                        0.8s
 => => sha256:db840d086b65cf73e0feea3bd0cf11063818114e466846ae3f2b2fb1a8c2b143 14.45MB / 14.45MB                                                  5.6s
 => => extracting sha256:6310eb16bf4251731feab01e8f633bf5e2d75a657ccad97f420b1f83cce457be                                                         4.7s
 => => extracting sha256:3678bb828654fcc3752f7a5eb63c5accfa00c97047252f25405285550d74a3fd                                                         1.0s
 => => extracting sha256:db840d086b65cf73e0feea3bd0cf11063818114e466846ae3f2b2fb1a8c2b143                                                         3.5s
 => => extracting sha256:f9efa1b83d065a7c5a3041582875b75d63c4ab3d4413514de8e413b51f90e91a                                                         0.1s
 => [internal] load build context                                                                                                                 0.1s
 => => transferring context: 800B                                                                                                                 0.0s
 => [2/4] WORKDIR /app                                                                                                                            9.7s
 => [3/4] COPY ex3-flash-sale.py .                                                                                                                0.2s
 => [4/4] RUN pip install --no-cache-dir flask gunicorn                                                                                          50.3s
 => exporting to image                                                                                                                            5.2s
 => => exporting layers                                                                                                                           3.8s
 => => exporting manifest sha256:74d37e2ec44b613069edf2b75b802aca1baf0aa659a1ccc21ec3a3cbca4d2b71                                                 0.0s
 => => exporting config sha256:3ee64aefb83c4f609f3a11df2f4b77c68d469e476d64304921a3738bba3401eb                                                   0.0s
 => => exporting attestation manifest sha256:34875f9caa4d55008189132dd06e6c7ff54fd2c525fa154aa5c4ab9b716a8c13                                     0.1s
 => => exporting manifest list sha256:aecdb925ac87211c2825dc7fd4dffd3a96eb57cc5f34325c5975efdcb16eadb5                                            0.0s
 => => naming to docker.io/adi18prasad/flashsale:1.0                                                                                              0.0s
 => => unpacking to docker.io/adi18prasad/flashsale:1.0                                                                                           0.9s

View build details: docker-desktop://dashboard/build/desktop-linux/desktop-linux/d1mwc68b36ruvgp819zh4s0s2
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment3> docker push adi18prasad/flashsale:1.0
The push refers to repository [docker.io/adi18prasad/flashsale]
f9efa1b83d06: Pushed 
3678bb828654: Pushed 
ca1a94d515af: Pushed 
15c75152d8b9: Pushed 
db840d086b65: Pushed 
90162d26b4c5: Pushed 
99bff7a9ea99: Pushed 
6310eb16bf42: Pushed 
1.0: digest: sha256:aecdb925ac87211c2825dc7fd4dffd3a96eb57cc5f34325c5975efdcb16eadb5 size: 856
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment3> minikube start --nodes=1
😄  minikube v1.38.1 on Microsoft Windows 11 Home Single Language 25H2
🎉  minikube 1.39.0 is available! Download it: https://github.com/kubernetes/minikube/releases/tag/v1.39.0
💡  To disable this notice, run: 'minikube config set WantUpdateNotification false'

✨  Automatically selected the docker driver. Other choices: hyperv, ssh
❗  Starting v1.39.0, minikube will default to "containerd" container runtime. See #21973 for more info.
📌  Using Docker Desktop driver with root privileges
👍  Starting "minikube" primary control-plane node in "minikube" cluster
🚜  Pulling base image v0.0.50 ...
🔥  Creating docker container (CPUs=2, Memory=3072MB) ... 
🐳  Preparing Kubernetes v1.35.1 on Docker 29.2.1 ... 
🔗  Configuring bridge CNI (Container Networking Interface) ...
🔎  Verifying Kubernetes components...
❗  Executing "docker container inspect minikube --format={{.State.Status}}" took an unusually long time: 2.5324111s
💡  Restarting the docker service may improve performance.
    ▪ Using image gcr.io/k8s-minikube/storage-provisioner:v5
🌟  Enabled addons: storage-provisioner, default-storageclass
🏄  Done! kubectl is now configured to use "minikube" cluster and "default" namespace by default
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment3> kubectl get nodes
NAME       STATUS   ROLES           AGE   VERSION
minikube   Ready    control-plane   36s   v1.35.1
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment3> kubectl apply -f flashsale-replicaset.yaml
replicaset.apps/flashsale-rs created
service/flashsale-svc created
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment3> minikube docker-env
$Env:DOCKER_TLS_VERIFY = "1"
$Env:DOCKER_HOST = "tcp://127.0.0.1:64818"
$Env:DOCKER_CERT_PATH = "C:\Users\adina\.minikube\certs"
$Env:MINIKUBE_ACTIVE_DOCKERD = "minikube"
# To point your shell to minikube's docker-daemon, run:
# & minikube -p minikube docker-env --shell powershell | Invoke-Expression
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment3> eval $(minikube docker-env)
eval : The term 'eval' is not recognized as the name of a cmdlet, function, script file, or operable program. Check the spelling of the name, or if a 
path was included, verify that the path is correct and try again.
At line:1 char:1
+ eval $(minikube docker-env)
+ ~~~~
    + CategoryInfo          : ObjectNotFound: (eval:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException
 
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment3> & minikube -p minikube docker-env --shell powershell | Invoke-Expression
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment3> docker build -t flask-app .
[+] Building 37.5s (10/10) FINISHED                                                                                                     docker:default
 => [internal] load build definition from Dockerfile                                                                                              0.2s
 => => transferring dockerfile: 227B                                                                                                              0.1s
 => [internal] load metadata for docker.io/library/python:3.11-slim                                                                               2.8s
 => [auth] library/python:pull token for registry-1.docker.io                                                                                     0.0s
 => [internal] load .dockerignore                                                                                                                 0.1s
 => => transferring context: 2B                                                                                                                   0.0s
 => [1/4] FROM docker.io/library/python:3.11-slim@sha256:9534e5a8e315485d4061ed659af0fd78a284c015f9b73661b41d6bab25604534                        23.5s
 => => resolve docker.io/library/python:3.11-slim@sha256:9534e5a8e315485d4061ed659af0fd78a284c015f9b73661b41d6bab25604534                         0.1s
 => => sha256:b8fe4ce3655e95f7f22c2a87d8e03a2f1f0cedc488a8e9adf18cc5a18cfdf401 5.49kB / 5.49kB                                                    0.0s
 => => sha256:6310eb16bf4251731feab01e8f633bf5e2d75a657ccad97f420b1f83cce457be 29.79MB / 29.79MB                                                  5.8s
 => => sha256:3678bb828654fcc3752f7a5eb63c5accfa00c97047252f25405285550d74a3fd 4.27MB / 4.27MB                                                    2.9s
 => => sha256:db840d086b65cf73e0feea3bd0cf11063818114e466846ae3f2b2fb1a8c2b143 14.45MB / 14.45MB                                                  3.7s
 => => sha256:9534e5a8e315485d4061ed659af0fd78a284c015f9b73661b41d6bab25604534 10.37kB / 10.37kB                                                  0.0s
 => => sha256:d1053354624536b044162aaab1e418bd000ea35184fb1ae098ab3166b1072e72 1.75kB / 1.75kB                                                    0.0s
 => => sha256:f9efa1b83d065a7c5a3041582875b75d63c4ab3d4413514de8e413b51f90e91a 249B / 249B                                                        3.3s
 => => extracting sha256:6310eb16bf4251731feab01e8f633bf5e2d75a657ccad97f420b1f83cce457be                                                         8.5s
 => => extracting sha256:3678bb828654fcc3752f7a5eb63c5accfa00c97047252f25405285550d74a3fd                                                         1.7s
 => => extracting sha256:db840d086b65cf73e0feea3bd0cf11063818114e466846ae3f2b2fb1a8c2b143                                                         6.2s
 => => extracting sha256:f9efa1b83d065a7c5a3041582875b75d63c4ab3d4413514de8e413b51f90e91a                                                         0.0s
 => [internal] load build context                                                                                                                 0.1s
 => => transferring context: 800B                                                                                                                 0.0s
 => [2/4] WORKDIR /app                                                                                                                            1.2s
 => [3/4] COPY ex3-flash-sale.py .                                                                                                                0.1s
 => [4/4] RUN pip install --no-cache-dir flask gunicorn                                                                                           7.2s
 => exporting to image                                                                                                                            0.7s
 => => exporting layers                                                                                                                           0.6s
 => => writing image sha256:dc35956cdcaaa76e827d4bfbf3472273807bfe6ce8c68f8b7267a4ce7e3ae8b8                                                      0.0s
 => => naming to docker.io/library/flask-app                                                                                                      0.0s

View build details: docker-desktop://dashboard/build/default/default/8asx199cg2i7dvs7wqo98siki
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment3> kubectl get pods
NAME                 READY   STATUS             RESTARTS   AGE
flashsale-rs-247zn   0/1     ErrImagePull       0          2m7s
flashsale-rs-4g687   0/1     ImagePullBackOff   0          2m7s
flashsale-rs-6pzrx   0/1     ImagePullBackOff   0          2m7s
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment3> kubectl get rs
NAME           DESIRED   CURRENT   READY   AGE
flashsale-rs   3         3         0       2m24s

(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment3> kubectl scale rs flashsale-rs --replicas=5
replicaset.apps/flashsale-rs scaled
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment3> kubectl get rs
NAME           DESIRED   CURRENT   READY   AGE
flashsale-rs   5         5         0       3m53s
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment3> kubectl get pods
NAME                 READY   STATUS             RESTARTS   AGE
flashsale-rs-247zn   0/1     ImagePullBackOff   0          4m4s
flashsale-rs-4g687   0/1     ImagePullBackOff   0          4m4s
flashsale-rs-6pzrx   0/1     ImagePullBackOff   0          4m4s
flashsale-rs-hx9xf   0/1     ImagePullBackOff   0          48s
flashsale-rs-rq4mx   0/1     ErrImagePull       0          48s
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment3> kubectl get pods                                                        
NAME                 READY   STATUS             RESTARTS   AGE
flashsale-rs-247zn   0/1     ImagePullBackOff   0          4m25s
flashsale-rs-4g687   0/1     ImagePullBackOff   0          4m25s
flashsale-rs-6pzrx   0/1     ImagePullBackOff   0          4m25s
flashsale-rs-hx9xf   0/1     ImagePullBackOff   0          69s
flashsale-rs-rq4mx   0/1     ErrImagePull       0          69s
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment3> kubectl delete pod flashsale-rs-247zn
pod "flashsale-rs-247zn" deleted from default namespace
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment3> kubectl get pods                     
NAME                 READY   STATUS             RESTARTS   AGE
flashsale-rs-4g687   0/1     ImagePullBackOff   0          4m56s
flashsale-rs-6pzrx   0/1     ImagePullBackOff   0          4m56s
flashsale-rs-hx9xf   0/1     ImagePullBackOff   0          100s
flashsale-rs-rq4mx   0/1     ImagePullBackOff   0          100s
flashsale-rs-s2cmh   0/1     ErrImagePull       0          8s
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment3> kubectl get pods -o wide
NAME                 READY   STATUS             RESTARTS   AGE    IP           NODE       NOMINATED NODE   READINESS GATES
flashsale-rs-4g687   0/1     ImagePullBackOff   0          5m8s   10.244.0.4   minikube   <none>           <none>
flashsale-rs-6pzrx   0/1     ImagePullBackOff   0          5m8s   10.244.0.6   minikube   <none>           <none>
flashsale-rs-hx9xf   0/1     ImagePullBackOff   0          112s   10.244.0.8   minikube   <none>           <none>
flashsale-rs-rq4mx   0/1     ImagePullBackOff   0          112s   10.244.0.7   minikube   <none>           <none>
flashsale-rs-s2cmh   0/1     ImagePullBackOff   0          20s    10.244.0.9   minikube   <none>           <none>
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment3> 