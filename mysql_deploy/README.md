[Using Kubernetes Local Persistent Volumes on Docker-Desktop](http://duffney.io/UsingKubernetesLocalPersistentVolumesDockerDesktop)


```bash
#run side-car mysql-client container
kubectl run -it --rm --image=mysql:5.6 --restart=Never mysql-client -- mysql -h mysql -ppassword

#mysql commands to run
create database teamcity collate utf8_bin;
create user teamcity identified by 'password';
grant all privileges on teamcity.* to teamcity;
grant process on *.* to teamcity;

#list contents of mysql volume
ls /tmp/teamcitydata
```