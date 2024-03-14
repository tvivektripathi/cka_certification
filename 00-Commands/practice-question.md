1. <details>
   <summary>Count the number of pods</summary>
   ```
   $ kubectl get pods
   ```
   </details>
1. <details>
   <summary>Count the number of replicasets</summary>
   ```
   $ kubectl get rs
   ```
   </details>
1. <details>
   <summary>Look at the count under the **`Desired`** column</summary>

   ```
   $ kubectl get rs
   ```
   </details>

1. Run the command **`kubectl describe replicaset`** and look under the containers section.
   
   <details>
   <summary>Look at the count under the **`Desired`** column</summary>
   
   ```
   $ kubectl describe replicaset (or)
   $ kubectl get rs -o wide
   ```
   </details>

1. Run the command **`kubectl get replicaset`** and look at the count under the **`Ready`** column

   <details>

   ```
   $ kubectl get repplicaset
   ```
   </details>

1. Run the command **`kubectl describe pods`** and look under the events section.
   
   <details>

   ```
   $ kubectl describe pods
   ```
   </details>

1. Run the command **`kubectl delete pod <podname>`**

   <details>

   ```
   $ kubectl delete pod new-replica-set-XXXX
   ```
   </details>

1. Run the command **`kubectl get pods`** and count the number of PODs
   
   <details>

   ```
   $ kubectl get pods
   ```
   </details>

1. ReplicaSets ensures that desired number of PODs always run

1. The value for **`apiVersion`** is incorrect. Find the correct apiVersion for ReplicaSet.

   Get the apiVersion for replicaset
   
   <details>

   ```
   $ kubectl explain replicaset|grep VERSION
   ```
   </details>

   Update the replicaset defination file with correct version and create a replicaset
    
   <details>

   ```
   $ kubectl create -f replicaset-defination-1.yaml
   ```
   </details>

1. The values for labels on lines 9 and 13 should match.
   <details>

   ```
   Selector matchLabels should match with POD labels - Update the replicaset-defination-2.yaml
   $ kubectl create -f replicaset-defination-2.yaml
   ```
   </details>

1. Run the command **`kubectl delete replicaset`**
   
   <details>

   ```
   $ kubectl delete replicaset replicaset-1
   $ kubectl delete rs replicaset-2
   ```
   </details>

1. Run the command **`kubectl edit replicaset new-replica-set`**, modify the image name to **`busybox`** and then save the file.
   
   <details>

   ```
   $ kubectl edit replicaset new-replica-set
   ```
   </details>

1. Run the command **`kubectl edit replicaset new-replica-set`**, modify the replicas and then save the file.
   
   <details>

   ```
   $ kubectl edit replicaset new-replica-set
   ```
   </details>

   Another way
   
   <details>
   
   ```
   $ kubectl scale --replicas=5 replicaset new-replica-set
   ```
   </details>

1. Run the command **`kubectl edit replicaset new-replica-set`**, modify the replicas and then save the file.

   <details>

   ```
   $ kubectl edit replicaset new-replica-set
   ```
   </details>

   Another way
   
   <details>

   ```
   $ kubectl scale --replicas=2 replicaset new-replica-set
   ```
   </details>
1. Run the command **`kubectl get pods`** and count the number of pods.
   
   <details>

   ```
   $ kubectl get pods
   ```
   </details>

1. Run the command **`kubectl get replicaset`** and count the number of ReplicaSets.
   
   <details>

   ```
   $ kubectl get replicaset (or)
   $ kubectl get rs
   ```
   </details>

1. Run the command **`kubectl get deployment`** and count the number of Deployments.
   
   <details>

   ```
   $ kubectl get deployment
   ```
   </details>

1. Run the command **`kubectl get deployment`** and count the number of Deployments.
   
   <details>

   ```
   $ kubectl get deployment
   ```
   </details>

1. Run the command **`kubectl get replicaset`** and count the number of ReplicaSets.
   
   <details>

   ```
   $ kubectl get replicaset (or)
   $ kubectl get rs
   ```
   </details>

1. Run the command **`kubectl get pods`** and count the number of PODs.
   
   <details>

   ```
   $ kubectl get pods
   ```
   </details>

1. Run the command **`kubectl get deployment`** and count the number of PODs.
   
   <details>

   ```
   $ kubectl get deployment
   ```
   </details>

1. Run the command **`kubectl describe deployment`** and look under the containers section.

   <details>

   ```
   $ kubectl describe deployment
   ```
   </details>

   Another way
   
   <details>

   ```
   $ kubectl get deployment -o wide
   ```
   </details>

1. Run the command **`kubectl describe pods`** and look under the events section.

   <details>

   ```
   $ kubectl describe pods
   ```
   </details>

1. Run the command **`kubectl describe pods`** and look under the events section.
   
   <details>

   ```
   $ kubectl describe pods
   ```
   </details>

1. The value for **`kind`** is incorrect. It should be **`Deployment`** with a capital **`D`**. Update the deployment defination and create the deployment.

   <details>

   ```
   $ kubectl create -f deployment-defination-1.yaml
   ```
   </details>

1. Run the command below command
 
   <details>

   ```
   $ kubectl create deployment httpd-frontend --image=httpd:2.4-alpine 
   $ kubectl scale deplyoment httpd-frontend --replicas=3
   ```
   </details>
1. Run the command **`kubectl get namespace`** and count the number of pods.
   
   <details>

   ```
   $ kubectl get namespace
   ```
   </details>

1. Run the command **`kubectl get pods --namespace=research`**
   
   <details>

   ```
   $ kubectl get pods --namespace=research
   ```
   </details>

1. Run the below command

   <details>

   ```
   $ kubectl run redis --image=redis --namespace=finance
   ```
   </details>

1. Run the command **`kubectl get pods --all-namespaces`**

   <details>

   ```
   $ kubectl get pods --all-namespaces
   ```
   </details>
1. Run the command **`kubectl get services`** and count the number of services.
  
  <details>

  ```
  $ kubectl get services
  ```
  </details>

1. Run the command **`kubectl get services`** and look at the Type column

  <details>

  ```
  $ kubectl get services
  ```
  </details>

1. Run the command **`kubectl describe service`** and look at TargetPort.

  <details>

  ```
  $ kubectl describe service|grep TargetPort
  ```
  </details>

1. Run the command **`kubectl describe service`** and look at Labels

  <details>

  ```
  $ kubectl describe service
  ```
  </details>

1. Run the command **`kubectl describe service`** and look at Endpoints
  
  <details>

  ```
  $ kubectl describe service
  ```
  </details>

1. Run the command **`kubectl get deployment`** and count the number of pods.

  <details>

  ```
  $ kubectl get deployment
  ```
  </details>

1. Run the command **`kubectl describe deployment`** and look under the containers section.

  <details>

  ```
  $ kubectl describe deployment
  ```
  </details>

1. Try to access the Web Application UI using the tab simple-webapp-ui above the terminal.

1. Update the given values in the service definition file and create the service.

  <details>

  ```
  $ kubectl create -f service-defination-1.yaml
  ```
  </details>

1. Use the command kubectl run nginx-pod --image=nginx:alpine
  
  <details>

  ```
  $ kubectl run nginx-pod --image=nginx:alpine
  ```
  </details>

1. Use the command kubectl run redis --image=redis:alpine -l tier=db

  <details>

  ```
  $ kubectl run redis --image=redis:alpine -l tier=db
  ```
  </details>

1. Run the command kubectl expose pod redis --port=6379 --name redis-service

  <details>

  ```
  $ kubectl expose pod redis --port=6379 --name redis-service
  ```
  </details>

1. Use the command kubectl create deployment webapp --image=kodekloud/webapp-color. The scale the webapp to 3 using command kubectl scale deployment/webapp --replicas=3

  <details>

  ```
  $ kubectl create deployment webapp --image=kodekloud/webapp-color
  $ kubectl scale deployment/webapp --replicas=3
  ```
  </details>

1. Run kubectl run custom-nginx --image=nginx --port=8080

  <details>

  ```
  $ kubectl run custom-nginx --image=nginx --port=8080
  ```
  </details>

1. Run kubectl create ns dev-ns
  
  <details>

  ```
  $ kubectl create ns dev-ns
  ```
  </details>

1. To create deployment

    <details>

    ```
    Step 1: Create the deployment YAML file
    $ kubectl create deployment redis-deploy --image redis --namespace=dev-ns --dry-run=client -o yaml > deploy.yaml
    $ kubectl create -f deploy.yaml

    Step 2: Edit the YAML file and add update the replicas to 2
    
    Step 3: Run kubectl apply -f deploy.yaml to create the deployment in the dev-ns namespace.
    $ kubectl apply -f deploy.yaml

    You can also use kubectl scale deployment or kubectl edit deployment to change the number of replicas once the object has been created.
    $ kubectl edit deployment redis-deploy
    $ kubectl scale deployment/redis-deploy --replicas=2 --namespace=dev-ns
    ```
    </details>

1. First create a YAML file for both the pod and service like this: kubectl run httpd --image=httpd:alpine --port=80 --expose

    <details>

    ```
    $ kubectl run httpd --image=httpd:alpine --port=80 --expose
    ```
    </details>

 
