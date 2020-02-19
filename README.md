# learn-helm

* learningapp contains simple kubernetes files 
* learning-chart has the same learningapp files with only a namepsace replacement through values  
* learningapp install an httpd exposing over nodeport
* helm packaging allows it to be deployed as many times passing a differnt value for namespace each time

### Example

helm install l learning-chart-0.1.0.tgz   
helm install l1 learning-chart-0.1.0.tgz --set namespace=learning1  
helm package xl-demo  
helm install xl-demo-0.1.0.tgz

### Setting up

#### Minikube requirements for hosting stack

At least 4 CPUS and 10Gigs Memory.  
```
mk config view
- cpus: 8
- dashboard: true
- ingress: true
- memory: 10240
- vm-driver: hyperkit

```

#### Create a mount to a folder that carries the license
/Users/amitmohleji/minikube-mount contains a folder xl-licenses that has licenses for XLD and XLR

``` 
mk addons enable ingress
mk mount /Users/amitmohleji/minikube-mount:/home/mount
```

#### Update hosts file on your machine to access each application. 
Get your minikube ip and use that.
Hosts entry

```
192.168.64.5 jenkins.xl xld.xl xlr.xl gogs.xl art.xl jboss.xl jadmin.xl apache.xl
```

#### Accessing servers
http://jenkins.xl/  
http://xld.xl/  
http://xlr.xl/   
etc..



