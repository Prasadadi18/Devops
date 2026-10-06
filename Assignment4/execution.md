                {da638e1b8a449514c3fda83ff50a3bffae4418b050cfacd87e5722071f497 5.40kB / 5.40kB                                                    0.0s
                    "Subnet": "172.18.0.0/16",                                                                                                    0.1s
                    "Gateway": "172.18.0.1"                                                                                                       0.0s
                }s\adina\OneDrive\Desktop\Devops\Devops\Assignment4>                                                                              0.0s
            ]
        },
        "Internal": false,
        "Attachable": false,
        "Ingress": false,
        "ConfigFrom": {
            "Network": ""
        },
        "ConfigOnly": false,
        "Options": {},
        "Labels": {},
        "Containers": {},
        "Status": {
            "IPAM": {
                "Subnets": {
                    "172.18.0.0/16": {
                        "IPsInUse": 3,
                        "DynamicIPsAvailable": 65533
                    }
                }
            }
        }
    }
]
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment4> docker build -t flask-api .                        
[+] Building 32.7s (10/10) FINISHED                                                                                                     docker:default
 => [internal] load build definition from Dockerfile                                                                                              0.1s
 => => transferring dockerfile: 514B                                                                                                              0.1s
 => [internal] load metadata for docker.io/library/python:3.9-slim                                                                                1.1s
 => [internal] load .dockerignore                                                                                                                 0.0s
 => => transferring context: 2B                                                                                                                   0.0s
 => [1/5] FROM docker.io/library/python:3.9-slim@sha256:2d97f6910b16bd338d3060f261f53f144965f755599aab1acda1e13cf1731b1b                         22.1s
 => => resolve docker.io/library/python:3.9-slim@sha256:2d97f6910b16bd338d3060f261f53f144965f755599aab1acda1e13cf1731b1b                          0.0s
 => => sha256:b3ec39b36ae8c03a3e09854de4ec4aa08381dfed84a9daa075048c2e3df3881d 1.29MB / 1.29MB                                                    1.4s
 => => sha256:fc74430849022d13b0d44b8969a953f842f59c6e9d1a0c2c83d710affa286c08 13.88MB / 13.88MB                                                  5.3s
 => => sha256:2d97f6910b16bd338d3060f261f53f144965f755599aab1acda1e13cf1731b1b 10.36kB / 10.36kB                                                  0.0s
 => => sha256:dad5b29e3506c35e0fd222736f4d4ef25d21b219acdd73f7bb41d59996ca8e0d 1.74kB / 1.74kB                                                    0.0s
 => => sha256:085da638e1b8a449514c3fda83ff50a3bffae4418b050cfacd87e5722071f497 5.40kB / 5.40kB                                                    0.0s
 => => sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d 29.78MB / 29.78MB                                                  5.0s
 => => sha256:ea56f685404adf81680322f152d2cfec62115b30dda481c2c450078315beb508 251B / 251B                                                        1.9s
 => => extracting sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d                                                         9.4s
 => => extracting sha256:b3ec39b36ae8c03a3e09854de4ec4aa08381dfed84a9daa075048c2e3df3881d                                                         0.9s
 => => extracting sha256:fc74430849022d13b0d44b8969a953f842f59c6e9d1a0c2c83d710affa286c08                                                         5.5s
 => => extracting sha256:ea56f685404adf81680322f152d2cfec62115b30dda481c2c450078315beb508                                                         0.0s
 => [internal] load build context                                                                                                                 0.0s
 => => transferring context: 443B                                                                                                                 0.0s
 => [2/5] WORKDIR /app                                                                                                                            0.2s
 => [3/5] COPY requirements.txt .                                                                                                                 0.1s
 => [4/5] COPY app.py .                                                                                                                           0.1s
 => [5/5] RUN pip install --no-cache-dir -r requirements.txt                                                                                      8.6s
 => exporting to image                                                                                                                            0.5s
 => => exporting layers                                                                                                                           0.4s
 => => writing image sha256:bf4969c58a0450b396cdc6c1b6ebc29cd7ea4cfa3dce44895e84936b6192a7d5                                                      0.0s
 => => naming to docker.io/library/flask-api                                                                                                      0.0s

View build details: docker-desktop://dashboard/build/default/default/m5b536kryrnedozw87um2wy0z
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment4> docker run -d --name mysql --net=my-bridge-net mysql:latest
Unable to find image 'mysql:latest' locally
latest: Pulling from library/mysql
30627cea5424: Pull complete 
7e887550bdc4: Pull complete 
35475b275575: Pull complete 
27683f99b921: Pull complete 
0bb65eb170f9: Pull complete 
e480dcc782ea: Pull complete 
1791a4d7fecf: Pull complete 
71fa527c6c68: Pull complete 
c4e766e27938: Pull complete 
feffc3e2a7dd: Pull complete 
Digest: sha256:66aec17cd21a956029b83f083b813073859e8355dc1a00e55df6ba02f0e32345
Status: Downloaded newer image for mysql:latest
9ee69072ca5021d77e32050a2dad49986eee4b7e4f3d095ef2bd1e31748edc99
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment4> docker run -d --name redis --net=my-bridge-net redis:latest
Unable to find image 'redis:latest' locally
latest: Pulling from library/redis
6310eb16bf42: Already exists 
9b30195f536d: Pull complete 
db0606565b61: Pull complete 
87650244ec3e: Pull complete 
5b7942a2dab1: Pull complete 
4f4fb700ef54: Pull complete 
b1de9b9d5a81: Pull complete 
Digest: sha256:298e5b3bc566bade82f46ad5511777a4a07a294097ce16ada2f6a42be5239df5
Status: Downloaded newer image for redis:latest
2c90a672a45d1d890da8d1f4ee243e3aa7dfafe2aa007b0b96d4667f30d29533
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment4> docker run -d --name flask --net=my-bridge-net -p 5001:5001 flask-api
e8f621e5c87e7b9d159f3cb2a13cea2b46ab80abf76a73c0666381a179a4483f
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment4> docker exec -it flask bash

What's next:
    Try Docker Debug for seamless, persistent debugging tools in any container or image → docker debug flask
    Learn more at https://docs.docker.com/go/debug-cli/
Error response from daemon: container e8f621e5c87e7b9d159f3cb2a13cea2b46ab80abf76a73c0666381a179a4483f is not running
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment4> docker logs flask
Traceback (most recent call last):
  File "/app/app.py", line 1, in <module>
    from flask import Flask, jsonify
  File "/usr/local/lib/python3.9/site-packages/flask/__init__.py", line 7, in <module>
    from .app import Flask as Flask
  File "/usr/local/lib/python3.9/site-packages/flask/app.py", line 28, in <module>
    from . import cli
  File "/usr/local/lib/python3.9/site-packages/flask/cli.py", line 18, in <module>
    from .helpers import get_debug_flag
  File "/usr/local/lib/python3.9/site-packages/flask/helpers.py", line 16, in <module>
    from werkzeug.urls import url_quote
ImportError: cannot import name 'url_quote' from 'werkzeug.urls' (/usr/local/lib/python3.9/site-packages/werkzeug/urls.py)
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment4> pip install flask
Requirement already satisfied: flask in c:\users\adina\anaconda3\lib\site-packages (3.0.0)
Requirement already satisfied: Werkzeug>=3.0.0 in c:\users\adina\anaconda3\lib\site-packages (from flask) (3.0.3)
Requirement already satisfied: Jinja2>=3.1.2 in c:\users\adina\anaconda3\lib\site-packages (from flask) (3.1.4)
Requirement already satisfied: itsdangerous>=2.1.2 in c:\users\adina\anaconda3\lib\site-packages (from flask) (2.2.0)
Requirement already satisfied: click>=8.1.3 in c:\users\adina\anaconda3\lib\site-packages (from flask) (8.3.3)
Requirement already satisfied: blinker>=1.6.2 in c:\users\adina\anaconda3\lib\site-packages (from flask) (1.6.2)
Requirement already satisfied: colorama in c:\users\adina\anaconda3\lib\site-packages (from click>=8.1.3->flask) (0.4.6)
Requirement already satisfied: MarkupSafe>=2.0 in c:\users\adina\anaconda3\lib\site-packages (from Jinja2>=3.1.2->flask) (2.1.3)
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment4> docker exec -it flask bash

What's next:
    Try Docker Debug for seamless, persistent debugging tools in any container or image → docker debug flask
    Learn more at https://docs.docker.com/go/debug-cli/
Error response from daemon: container e8f621e5c87e7b9d159f3cb2a13cea2b46ab80abf76a73c0666381a179a4483f is not running
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment4> docker exec -it flask bash

What's next:
    Try Docker Debug for seamless, persistent debugging tools in any container or image → docker debug flask
    Learn more at https://docs.docker.com/go/debug-cli/
Error response from daemon: container e8f621e5c87e7b9d159f3cb2a13cea2b46ab80abf76a73c0666381a179a4483f is not running
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment4> docker exec -it flask bash

What's next:
    Try Docker Debug for seamless, persistent debugging tools in any container or image → docker debug flask
    Learn more at https://docs.docker.com/go/debug-cli/
error during connect: Get "https://127.0.0.1:64818/v1.54/containers/flask/json": dial tcp 127.0.0.1:64818: connectex: No connection could be made because the target machine actively refused it.
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment4> docker context use default
default
Current context is now "default"
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment4> docker exec -it flask bash

What's next:
    Try Docker Debug for seamless, persistent debugging tools in any container or image → docker debug flask
    Learn more at https://docs.docker.com/go/debug-cli/
error during connect: Get "https://127.0.0.1:64818/v1.54/containers/flask/json": dial tcp 127.0.0.1:64818: connectex: No connection could be made because the target machine actively refused it.
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment4> Remove-Item Env:\DOCKER_HOST, Env:\DOCKER_TLS_VERIFY, Env:\DOCKER_CERT_PATH, Env:\MINIKUBE_ACTIVE_DOCKERD -ErrorAction SilentlyContinue
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment4> docker exec -it flask bash                                                        
                                                     
What's next:
    Try Docker Debug for seamless, persistent debugging tools in any container or image → docker debug flask
    Learn more at https://docs.docker.com/go/debug-cli/
Error response from daemon: No such container: flask
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment4> ocker ps -a
ocker : The term 'ocker' is not recognized as the name of a cmdlet, function, script file, or operable program. Check the spelling of the name, or if 
a path was included, verify that the path is correct and try again.
At line:1 char:1
+ ocker ps -a
+ ~~~~~
    + CategoryInfo          : ObjectNotFound: (ocker:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException
 
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment4> docker ps -a
CONTAINER ID   IMAGE                                 COMMAND                  CREATED          STATUS                        PORTS     NAMES
cb5fb5f10b91   gcr.io/k8s-minikube/kicbase:v0.0.50   "/usr/local/bin/entr…"   30 minutes ago   Exited (137) 2 minutes ago              minikube
2c164d258cf9   postgres:15                           "docker-entrypoint.s…"   2 months ago     Exited (0) 42 minutes ago               learndb_postgres
c4405eb92b32   redis:7                               "docker-entrypoint.s…"   2 months ago     Exited (0) 42 minutes ago               learndb_redis
9763cf00307f   ghcr.io/engineer-man/piston           "docker-entrypoint.s…"   2 months ago     Exited (137) 42 minutes ago             piston_api
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment4> docker build -t flask-api .
[+] Building 16.5s (11/11) FINISHED                                                                                                     docker:default
 => [internal] load build definition from Dockerfile                                                                                              0.1s
 => => transferring dockerfile: 514B                                                                                                              0.0s
 => [internal] load metadata for docker.io/library/python:3.9-slim                                                                                2.2s
 => [auth] library/python:pull token for registry-1.docker.io                                                                                     0.0s
 => [internal] load .dockerignore                                                                                                                 0.1s
 => => transferring context: 2B                                                                                                                   0.0s
 => [1/5] FROM docker.io/library/python:3.9-slim@sha256:2d97f6910b16bd338d3060f261f53f144965f755599aab1acda1e13cf1731b1b                          0.1s
 => => resolve docker.io/library/python:3.9-slim@sha256:2d97f6910b16bd338d3060f261f53f144965f755599aab1acda1e13cf1731b1b                          0.1s
 => [internal] load build context                                                                                                                 0.1s
 => => transferring context: 465B                                                                                                                 0.0s
 => CACHED [2/5] WORKDIR /app                                                                                                                     0.0s
 => [3/5] COPY requirements.txt .                                                                                                                 0.1s
 => [4/5] COPY app.py .                                                                                                                           0.1s
 => [5/5] RUN pip install --no-cache-dir -r requirements.txt                                                                                     11.0s
 => exporting to image                                                                                                                            3.5s 
 => => exporting layers                                                                                                                           1.8s 
 => => exporting manifest sha256:678c2195f238a10893a6af8ccdc1ce0dbeddb7a8f637ccbea249a2535730c4c8                                                 0.0s 
 => => exporting config sha256:6aa2a689f6a2d40a3fc33f092f62c57785649ccee8e08005a9763c3c69a075c8                                                   0.0s 
 => => exporting attestation manifest sha256:734fa3b3e8ed72450817da349c4ba7dd0fdd23672c97c9c12f710c0a392faf8e                                     0.1s 
 => => exporting manifest list sha256:052800501871f1be684dccd5eddad2a2a6d28e7b2b6fd7df26d4679efeea515a                                            0.0s 
 => => naming to docker.io/library/flask-api:latest                                                                                               0.0s
 => => unpacking to docker.io/library/flask-api:latest                                                                                            1.4s

View build details: docker-desktop://dashboard/build/default/default/63d02nu4ct44xnv1qa33jjmez
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment4> docker network create --driver bridge my-bridge-net
>> docker run -d --name mysql --net=my-bridge-net mysql:latest
>> docker run -d --name redis --net=my-bridge-net redis:latest
>> docker run -d --name flask --net=my-bridge-net -p 5001:5001 flask-api
819bbdcef0ac3d93e31b645e0440420bc563715c850c9197fb1b86d75b368522
Unable to find image 'mysql:latest' locally
latest: Pulling from library/mysql
30627cea5424: Pull complete 
feffc3e2a7dd: Pull complete 
7e887550bdc4: Pull complete 
27683f99b921: Pull complete 
35475b275575: Pull complete 
0bb65eb170f9: Pull complete 
e480dcc782ea: Pull complete 
71fa527c6c68: Pull complete 
c4e766e27938: Pull complete 
1791a4d7fecf: Pull complete 
81ee3e1129f4: Download complete 
808810e42158: Download complete 
Digest: sha256:66aec17cd21a956029b83f083b813073859e8355dc1a00e55df6ba02f0e32345
Status: Downloaded newer image for mysql:latest
d9a719d866510d8a33f8ebe2191638866d4c3967850e277fae299a08805742e5
Unable to find image 'redis:latest' locally
latest: Pulling from library/redis
4f4fb700ef54: Pull complete 
b1de9b9d5a81: Pull complete 
87650244ec3e: Pull complete 
db0606565b61: Pull complete 
9b30195f536d: Pull complete 
5b7942a2dab1: Pull complete 
bc63621f6444: Download complete 
fce2fbb27b14: Download complete 
Digest: sha256:298e5b3bc566bade82f46ad5511777a4a07a294097ce16ada2f6a42be5239df5
Status: Downloaded newer image for redis:latest
d7d830bf1ae5d866d32ac24db54d4ba2dab1254e6d2272e4138fecc63f7c8f6e
84864e212bc3932cc297b5be4cc4a3eb7feac1ae5afe5a94fcf445b591fe57ef
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment4> docker ps
CONTAINER ID   IMAGE          COMMAND                  CREATED          STATUS          PORTS      NAMES
d7d830bf1ae5   redis:latest   "docker-entrypoint.s…"   38 seconds ago   Up 34 seconds   6379/tcp   redis
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment4> docker ps
CONTAINER ID   IMAGE          COMMAND                  CREATED          STATUS          PORTS      NAMES
d7d830bf1ae5   redis:latest   "docker-entrypoint.s…"   48 seconds ago   Up 44 seconds   6379/tcp   redis
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment4> docker run -d --name mysql --net=my-bridge-net -e MYSQL_ROOT_PASSWORD=secret mysql:latest

What's next:
    Debug this container error with Gordon → docker ai "help me fix this container error"
docker: Error response from daemon: Conflict. The container name "/mysql" is already in use by container "d9a719d866510d8a33f8ebe2191638866d4c3967850e277fae299a08805742e5". You have to remove (or rename) that container to be able to reuse that name.

Run 'docker run --help' for more information
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment4> docker rm -f mysql
mysql
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment4> docker run -d --name mysql --net=my-bridge-net -e MYSQL_ROOT_PASSWORD=secret mysql:latest
20743d10eb7915d19abc893aa812dbc4b9050a0b04f9bea3f30f14dc26d6f801
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment4> docker ps                                                                         
CONTAINER ID   IMAGE          COMMAND                  CREATED          STATUS          PORTS                 NAMES
20743d10eb79   mysql:latest   "docker-entrypoint.s…"   28 seconds ago   Up 24 seconds   3306/tcp, 33060/tcp   mysql
d7d830bf1ae5   redis:latest   "docker-entrypoint.s…"   2 minutes ago    Up 2 minutes    6379/tcp              redis
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment4> docker build -t flask-api .
[+] Building 3.0s (11/11) FINISHED                                                                                                      docker:default
 => [internal] load build definition from Dockerfile                                                                                              0.1s
 => => transferring dockerfile: 514B                                                                                                              0.0s
 => [internal] load metadata for docker.io/library/python:3.9-slim                                                                                1.8s
 => [auth] library/python:pull token for registry-1.docker.io                                                                                     0.0s
 => [internal] load .dockerignore                                                                                                                 0.0s
 => => transferring context: 2B                                                                                                                   0.0s
 => [1/5] FROM docker.io/library/python:3.9-slim@sha256:2d97f6910b16bd338d3060f261f53f144965f755599aab1acda1e13cf1731b1b                          0.1s
 => => resolve docker.io/library/python:3.9-slim@sha256:2d97f6910b16bd338d3060f261f53f144965f755599aab1acda1e13cf1731b1b                          0.1s
 => [internal] load build context                                                                                                                 0.0s
 => => transferring context: 63B                                                                                                                  0.0s
 => CACHED [2/5] WORKDIR /app                                                                                                                     0.0s
 => CACHED [3/5] COPY requirements.txt .                                                                                                          0.0s
 => CACHED [4/5] COPY app.py .                                                                                                                    0.0s
 => CACHED [5/5] RUN pip install --no-cache-dir -r requirements.txt                                                                               0.0s
 => exporting to image                                                                                                                            0.7s
 => => exporting layers                                                                                                                           0.0s
 => => exporting manifest sha256:678c2195f238a10893a6af8ccdc1ce0dbeddb7a8f637ccbea249a2535730c4c8                                                 0.0s
 => => exporting config sha256:6aa2a689f6a2d40a3fc33f092f62c57785649ccee8e08005a9763c3c69a075c8                                                   0.0s
 => => exporting attestation manifest sha256:81768c415be0b68b7154d9b595061d4a88644d2fa9649b7e76dd660c514553f1                                     0.1s
 => => exporting manifest list sha256:6920245b79080ef3a34b675298abbdfbdba1e628b6fa3658e3aa5498c994a5b0                                            0.0s
 => => naming to docker.io/library/flask-api:latest                                                                                               0.0s
 => => unpacking to docker.io/library/flask-api:latest                                                                                            0.0s

View build details: docker-desktop://dashboard/build/default/default/n9w2zij94g6sxfxv2x4ktvcke
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment4> docker run -d --name flask --net=my-bridge-net -p 5001:5001 flask-api

What's next:
    Debug this container error with Gordon → docker ai "help me fix this container error"
docker: Error response from daemon: Conflict. The container name "/flask" is already in use by container "84864e212bc3932cc297b5be4cc4a3eb7feac1ae5afe5a94fcf445b591fe57ef". You have to remove (or rename) that container to be able to reuse that name.

Run 'docker run --help' for more information
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment4> docker rm -f flask
flask
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment4> docker run -d --name flask --net=my-bridge-net -p 5001:5001 flask-api
22f368f29f9ad0296b82b222fc297bacb1d8cd6f950f23cc0ca7d69bf09c4448
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment4> docker ps                                                            
CONTAINER ID   IMAGE          COMMAND                  CREATED              STATUS              PORTS                 NAMES
20743d10eb79   mysql:latest   "docker-entrypoint.s…"   About a minute ago   Up About a minute   3306/tcp, 33060/tcp   mysql
d7d830bf1ae5   redis:latest   "docker-entrypoint.s…"   3 minutes ago        Up 3 minutes        6379/tcp              redis
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment4> docker logs flask
Traceback (most recent call last):
  File "/app/app.py", line 1, in <module>
    from flask import Flask, jsonify
  File "/usr/local/lib/python3.9/site-packages/flask/__init__.py", line 7, in <module>
    from .app import Flask as Flask
  File "/usr/local/lib/python3.9/site-packages/flask/app.py", line 28, in <module>
    from . import cli
  File "/usr/local/lib/python3.9/site-packages/flask/cli.py", line 18, in <module>
    from .helpers import get_debug_flag
  File "/usr/local/lib/python3.9/site-packages/flask/helpers.py", line 16, in <module>
    from werkzeug.urls import url_quote
ImportError: cannot import name 'url_quote' from 'werkzeug.urls' (/usr/local/lib/python3.9/site-packages/werkzeug/urls.py)
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment4> docker build -t flask-api .                                          
[+] Building 32.5s (10/10) FINISHED                                                                                                     docker:default
 => [internal] load build definition from Dockerfile                                                                                              2.7s
 => => transferring dockerfile: 514B                                                                                                              2.2s
 => [internal] load metadata for docker.io/library/python:3.9-slim                                                                                2.1s
 => [internal] load .dockerignore                                                                                                                 0.0s
 => => transferring context: 2B                                                                                                                   0.0s
 => [1/5] FROM docker.io/library/python:3.9-slim@sha256:2d97f6910b16bd338d3060f261f53f144965f755599aab1acda1e13cf1731b1b                          0.1s
 => => resolve docker.io/library/python:3.9-slim@sha256:2d97f6910b16bd338d3060f261f53f144965f755599aab1acda1e13cf1731b1b                          0.1s
 => [internal] load build context                                                                                                                 0.1s
 => => transferring context: 120B                                                                                                                 0.0s
 => CACHED [2/5] WORKDIR /app                                                                                                                     0.0s
 => [3/5] COPY requirements.txt .                                                                                                                 0.2s
 => [4/5] COPY app.py .                                                                                                                           0.3s
 => [5/5] RUN pip install --no-cache-dir -r requirements.txt                                                                                     22.8s
 => exporting to image                                                                                                                            3.3s 
 => => exporting layers                                                                                                                           1.7s 
 => => exporting manifest sha256:0282d03a7a04860424ec362f272222869261a350d576ab060c4f5dec9e05cc7b                                                 0.0s 
 => => exporting config sha256:73cd340c499965430aa4d8428d45c6178840308673bf12410d9a16b613968c8a                                                   0.0s 
 => => exporting attestation manifest sha256:77a1868256b9e5542f4cd58d14f573edddf174890740f943f4b42db1fb970fce                                     0.0s 
 => => exporting manifest list sha256:43364fc62d0686cdededa12d1478918798098f21d991c38224f7ec1dff30d66a                                            0.0s 
 => => naming to docker.io/library/flask-api:latest                                                                                               0.0s
 => => unpacking to docker.io/library/flask-api:latest                                                                                            1.3s

View build details: docker-desktop://dashboard/build/default/default/coay1ivhhrrobzbfh28sk42sz
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment4> docker rm -f flask
flask
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment4> docker run -d --name flask --net=my-bridge-net -p 5001:5001 flask-api
1ed9c44dda80b740d4640d1e97c7cea681481ddb356f83e00bcd8c503eefe48a
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment4> docker logs flask                                                    
 * Serving Flask app 'app' (lazy loading)
 * Environment: production
   WARNING: This is a development server. Do not use it in a production deployment.
   Use a production WSGI server instead.
 * Debug mode: on
WARNING: This is a development server. Do not use it in a production deployment. Use a production WSGI server instead.
 * Running on http://127.0.0.1:5001
Press CTRL+C to quit
 * Restarting with stat
 * Debugger is active!
 * Debugger PIN: 918-027-918
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment4> docker ps
CONTAINER ID   IMAGE          COMMAND                  CREATED          STATUS          PORTS                                         NAMES
1ed9c44dda80   flask-api      "python app.py"          42 seconds ago   Up 39 seconds   0.0.0.0:5001->5001/tcp, [::]:5001->5001/tcp   flask
20743d10eb79   mysql:latest   "docker-entrypoint.s…"   4 minutes ago    Up 4 minutes    3306/tcp, 33060/tcp                           mysql
d7d830bf1ae5   redis:latest   "docker-entrypoint.s…"   6 minutes ago    Up 6 minutes    6379/tcp                                      redis
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment4> docker exec -it flask bash
root@1ed9c44dda80:/app# ping -c 3 mysql
bash: ping: command not found
root@1ed9c44dda80:/app# apt-get update && apt-get install -y iputils-ping
Get:1 http://deb.debian.org/debian trixie InRelease [140 kB]
Get:2 http://deb.debian.org/debian trixie-updates InRelease [47.3 kB]
Get:3 http://deb.debian.org/debian-security trixie-security InRelease [43.4 kB]
Get:4 http://deb.debian.org/debian trixie/main amd64 Packages [9673 kB]
Get:5 http://deb.debian.org/debian trixie-updates/main amd64 Packages [4412 B]
Get:6 http://deb.debian.org/debian-security trixie-security/main amd64 Packages [251 kB]
Fetched 10.2 MB in 6s (1844 kB/s)                    
Reading package lists... Done
N: Repository 'http://deb.debian.org/debian trixie InRelease' changed its 'Version' value from '13.1' to '13.6'
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following additional packages will be installed:
  libidn2-0 libunistring5 linux-sysctl-defaults
The following NEW packages will be installed:
  iputils-ping libidn2-0 libunistring5 linux-sysctl-defaults
0 upgraded, 4 newly installed, 0 to remove and 25 not upgraded.
Need to get 643 kB of archives.
After this operation, 2810 kB of additional disk space will be used.
Get:1 http://deb.debian.org/debian trixie/main amd64 libunistring5 amd64 1.3-2 [477 kB]
Get:2 http://deb.debian.org/debian trixie/main amd64 libidn2-0 amd64 2.3.8-2 [109 kB]
Get:3 http://deb.debian.org/debian trixie/main amd64 iputils-ping amd64 3:20240905-3 [51.2 kB]
Get:4 http://deb.debian.org/debian trixie/main amd64 linux-sysctl-defaults all 4.12.1 [5724 B]
Fetched 643 kB in 0s (2709 kB/s)           
debconf: unable to initialize frontend: Dialog
debconf: (No usable dialog-like program is installed, so the dialog based frontend cannot be used. at /usr/share/perl5/Debconf/FrontEnd/Dialog.pm line 79, <STDIN> line 4.)
debconf: falling back to frontend: Readline
debconf: unable to initialize frontend: Readline
debconf: (Can't locate Term/ReadLine.pm in @INC (you may need to install the Term::ReadLine module) (@INC entries checked: /etc/perl /usr/local/lib/x86_64-linux-gnu/perl/5.40.1 /usr/local/share/perl/5.40.1 /usr/lib/x86_64-linux-gnu/perl5/5.40 /usr/share/perl5 /usr/lib/x86_64-linux-gnu/perl-base /usr/lib/x86_64-linux-gnu/perl/5.40 /usr/share/perl/5.40 /usr/local/lib/site_perl) at /usr/share/perl5/Debconf/FrontEnd/Readline.pm line 8, <STDIN> line 4.)
debconf: falling back to frontend: Teletype
Selecting previously unselected package libunistring5:amd64.
(Reading database ... 5644 files and directories currently installed.)
Preparing to unpack .../libunistring5_1.3-2_amd64.deb ...
Unpacking libunistring5:amd64 (1.3-2) ...
Selecting previously unselected package libidn2-0:amd64.
Preparing to unpack .../libidn2-0_2.3.8-2_amd64.deb ...
Unpacking libidn2-0:amd64 (2.3.8-2) ...
Selecting previously unselected package iputils-ping.
Preparing to unpack .../iputils-ping_3%3a20240905-3_amd64.deb ...
Unpacking iputils-ping (3:20240905-3) ...
Selecting previously unselected package linux-sysctl-defaults.
Preparing to unpack .../linux-sysctl-defaults_4.12.1_all.deb ...
Unpacking linux-sysctl-defaults (4.12.1) ...
Setting up linux-sysctl-defaults (4.12.1) ...
Setting up libunistring5:amd64 (1.3-2) ...
Setting up libidn2-0:amd64 (2.3.8-2) ...
Setting up iputils-ping (3:20240905-3) ...
Processing triggers for libc-bin (2.41-12) ...
root@1ed9c44dda80:/app# ping -c 3 mysql
PING mysql (172.19.0.3) 56(84) bytes of data.
64 bytes from mysql.my-bridge-net (172.19.0.3): icmp_seq=1 ttl=64 time=7.31 ms
64 bytes from mysql.my-bridge-net (172.19.0.3): icmp_seq=2 ttl=64 time=1.52 ms
64 bytes from mysql.my-bridge-net (172.19.0.3): icmp_seq=3 ttl=64 time=0.191 ms

--- mysql ping statistics ---
3 packets transmitted, 3 received, 0% packet loss, time 1998ms
rtt min/avg/max/mdev = 0.191/3.004/7.306/3.089 ms
root@1ed9c44dda80:/app# ping -c 3 redis
PING redis (172.19.0.2) 56(84) bytes of data.
64 bytes from redis.my-bridge-net (172.19.0.2): icmp_seq=1 ttl=64 time=18.4 ms
64 bytes from redis.my-bridge-net (172.19.0.2): icmp_seq=2 ttl=64 time=0.162 ms
64 bytes from redis.my-bridge-net (172.19.0.2): icmp_seq=3 ttl=64 time=0.190 ms

--- redis ping statistics ---
3 packets transmitted, 3 received, 0% packet loss, time 1999ms
rtt min/avg/max/mdev = 0.162/6.266/18.446/8.612 ms
root@1ed9c44dda80:/app# ping  redis
PING redis (172.19.0.2) 56(84) bytes of data.
64 bytes from redis.my-bridge-net (172.19.0.2): icmp_seq=1 ttl=64 time=0.922 ms
64 bytes from redis.my-bridge-net (172.19.0.2): icmp_seq=2 ttl=64 time=0.157 ms
64 bytes from redis.my-bridge-net (172.19.0.2): icmp_seq=3 ttl=64 time=0.152 ms
64 bytes from redis.my-bridge-net (172.19.0.2): icmp_seq=4 ttl=64 time=0.206 ms
64 bytes from redis.my-bridge-net (172.19.0.2): icmp_seq=5 ttl=64 time=0.262 ms
64 bytes from redis.my-bridge-net (172.19.0.2): icmp_seq=6 ttl=64 time=0.464 ms
64 bytes from redis.my-bridge-net (172.19.0.2): icmp_seq=7 ttl=64 time=0.180 ms
64 bytes from redis.my-bridge-net (172.19.0.2): icmp_seq=8 ttl=64 time=0.249 ms
64 bytes from redis.my-bridge-net (172.19.0.2): icmp_seq=9 ttl=64 time=0.159 ms
^C
--- redis ping statistics ---
9 packets transmitted, 9 received, 0% packet loss, time 7992ms
rtt min/avg/max/mdev = 0.152/0.305/0.922/0.236 ms
root@1ed9c44dda80:/app# docker stop mysql redis flask && docker rm mysql redis flask
bash: docker: command not found
root@1ed9c44dda80:/app# exit
exit

What's next:
    Try Docker Debug for seamless, persistent debugging tools in any container or image → docker debug flask
    Learn more at https://docs.docker.com/go/debug-cli/
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment4> docker stop mysql redis flask && docker rm mysql redis flask
At line:1 char:31
+ docker stop mysql redis flask && docker rm mysql redis flask
+                               ~~
The token '&&' is not a valid statement separator in this version.
    + CategoryInfo          : ParserError: (:) [], ParentContainsErrorRecordException
    + FullyQualifiedErrorId : InvalidEndOfLine
 
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment4> docker stop mysql redis flask                               
mysql
redis
flask
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment4> docker rm mysql redis flask                                 
mysql
redis
flask
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment4> docker network rm my-bridge-net
my-bridge-net
(base) PS C:\Users\adina\OneDrive\Desktop\Devops\Devops\Assignment4>