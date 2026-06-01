----------------------------- **Important CMD's to remember** -------------------------------------------

•	kubectl api-resources -> All Objects are shown  
• kubectl api-resources --namespace==true --> Objects only at namespace level  
• kubectl api-resources --namespace==false --> Objects only at cluster level
•	kubectl get nodes -> will give the number of nodes connected to it

•	kubectl create ns (namespace) --> A New Namespace is created  
• kubectl get ns --> All available namespaces are shown



• kubectl get nodes
•
•
•


•	kubectl get pods --> pods in default namespace  
• kubectl get po -all-namespaces --> Shows all pods in all namespaces  
• kubectl get pods -n (namespace)  
•	kubectl get pods -o wide -n (namespace) --> pods are shown along with the node details  
• 
• kubectl get all -n (namespace)  
• kubectl desc pod (podname/podID) -n (namespace)  

•	kubectl apply  
•	kubectl apply -f (filename.yaml) --dry-run=client --> Its checks for any syntax errors (Image version is not validated)  
•	kubectl apply -f (filename.yaml) --> POD is created


•	kubectl exec --> Used to go inside the container of a POD  
•	kubectl exec [POD_NAME] [-c CONTAINER_NAME] [FLAGS] -- [COMMAND] [ARGS...]

•	kubectl exec my-pod -- ls /app	--> Run a single command  
•	kubectl exec -it my-pod -- /bin/bash --> Open interactive bash shell  
•	kubectl exec my-pod -c my-container -- date --> Exec into a specific container  
•	kubectl exec my-pod -- env --> Check environment variables


• kubectl delete po (podname) --> Delete the POD  
•
•
•
•








********************************** **Docker** ************************************

• docker  
• docker -v (Checks for the version)  

• docker images (shows all the images) / docker images ls  
• docker ps (display the process ) / docker ps -a (display all, Running stoppedm paused containers)  
• docker info (Client side / server side - details shown, depending on permission)  
• pwd (/home/ubuntu)  
Note: ubuntu is the default user  -> we need to add that user to the docker group - to get permission to view server side  


Add:  
sudo usermod -ag docker ubuntu  
              (apend to group) (group name) (username)  
exit  
reconnect to server  
docker images   
docker ps  
docker info  
ps -ef | grep -i "dockerd" -> docker demon process running in the background  
docker  
docker pull ubuntu:latest  
docker rmi  

• 


• docker run  
• docker run -d -p 80:80 --name (containerName)  nginx:latest (default latest version are pulled) nginx:1.9(version of Base Image)  
• 

•

