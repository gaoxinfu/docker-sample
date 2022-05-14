



```java
gaoxinfudeMacBook-Pro:nexus gaoxinfu$  docker pull jenkins/jenkins:lts
lts: Pulling from jenkins/jenkins
6aefca2dc61d: Pull complete 
e1108b695755: Pull complete 
4985c9eaee97: Pull complete 
8228d7831e76: Pull complete 
9519512ddfd4: Pull complete 
0733f6b69c1e: Pull complete 
b336c88402cb: Pull complete 
cb7dc9e53b9a: Pull complete 
e07562e27aae: Pull complete 
459456f5f3a7: Pull complete 
bba697df7a23: Pull complete 
fd343a6d7b0a: Pull complete 
064f97281dfa: Pull complete 
105e1c5c62b9: Pull complete 
47468e3b9259: Pull complete 
0c33547f2be5: Pull complete 
6ae3378125de: Pull complete 
Digest: sha256:3dec77ef6636c4f4068f855fb2857bd3e8942b12bdd9c7429bd64ab8bc392527
Status: Downloaded newer image for jenkins/jenkins:lts
docker.io/jenkins/jenkins:lts
gaoxinfudeMacBook-Pro:nexus gaoxinfu$ docker run -p 8090:8080 --name jenkins -u root -v /Users/gaoxinfu/data/docker/jenkins:/var/jenkins_home -d jenkins/jenkins:lts;
ba2fe88dff5dd4383b46eff43c0b5f83594410e0abf418e78e64ada253a36cfb
gaoxinfudeMacBook-Pro:nexus gaoxinfu$ 
```

**启动可能有点慢，需要等待一下**

http://localhost:8090



