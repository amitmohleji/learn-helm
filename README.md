# learn-helm

* learningapp contains simple kubernetes files 
* learning-chart has the same learningapp files with only a namepsace replacement through values  
* learningapp install an httpd exposing over nodeport
* helm packaging allows it to be deployed as many times passing a differnt value for namespace each time

### Example

helm install l learning-chart-0.1.0.tgz 
helm install l1 learning-chart-0.1.0.tgz --set namespace=learning1