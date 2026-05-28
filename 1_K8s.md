************* Kubernetes *******************

----------------------------------------- **General and Quick:** ----------------------------------------------
1. Explain Kubernetes architecture (master vs worker nodes).?
2. How Cluster is setup ? --> (On-Prem and EKS)
3. How nodes are connected to Cluster ?
4. What are Types of Clusters? -> Self Managed(Minikube, Kubeadm) and Cloud Managed(AWS-EKS, Azure-AKS, GCP-GKE)
5. Basic / Important K8s Objects to know ? ()



**General**

1. What is Reclaim Policies ? --> Retain(Default), Delete, Recycle(deprecated)
2. What is Equality Based ReplicaSet, Set Based ReplicaSet ?
3. 


------------------------------------ **Pods, Nodes, Cluster, Scheduling** --------------------------------------------

1. What is Cluster ?
2. What is POD ?
3. What is Node ?
4. What are Labels and Selectors?
5. What are Request and Limits ?
6. What are Liveness Probe and Readiness Probe ?
7. What is a demonset ?
8. 
9. 


1. What is Static POD and How it works.? Usecases or examples.
2. Init containers and Sidecar Containers ?
3. 


1. Node selector, Node Affinity, POD affinity, POD anti affinity ; Soft rule and Hard rule
2. Node Maintance --> Cordon, Drain, Uncordon

1. Cluster Upgrade ?
2. Node group upgrade ?
3. 

----------------------------------- **Security, Networking, Services:** -----------------------------------

1. ConfigMaps and secerts
2.
3.
4.
5.

1. What is a Service.
7. What are the types of Services.? --> (ClusterIP, NodePort, LoadBalancer)
8. 
9.
10.


1. What is Network Policies and how is it used.
7. Types of Rules ? --> (Ingress Rules, Egress Rules, Policy Type)
8. What is NodeExpoter ?
9. 
10. 



**RBAC** - Roll-based access controll
1. Role
2. Role Binding
3. Cluster Role
4. Cluster RoleBinding


1. How POD <--> POD communicate ? -->
2. How NameSpace <--> NameSpace communicate ? -->
3. How services communicate? --> can say: REST APIs, Internal Kubernetes services, Sometimes Kafka/RabbitMQ for async communication.

4. How did pods communicate securely? --> TLS, Network policies, Internal service communication

5. How did you handle sensitive customer data? --> Need: secrets, encryption, restricted access, RBAC


--------------------------------------------- **Scaling, Volumes** -------------------------------------------
1. What is Vertical scaling ?
2. What is Horizontal scaling ?
3. What is POD autoscaling ?  --> VPA & HPA
4. What is Server autoscaling / cluster autoscaling ? 
5. 
6.   HPA -> Horizontal pod AutoScaling



1. why volumes ? --> Host Path volumes, NFS server, PV, PVC & 
2. what volumes are you using ? 
3. Reclaim policies --> (Retain(default), Delete, Recycle(deprecated)
4. Storage Classes

------------------------------------------ **HELM Charts** --------------------------------------------

1. Helm chart Setup?
2. Create chart?
3. Deploy chart ?
4. Convert to tar file.?
5. create a chart from tar ?
6. 
----------------------------------- **Deployment Strategies** -----------------------------------------

1. Rolling Updates
2. Blue-green
3. Canary

1. Rollback strategy ?
2. How traffic is mapped / moved from one - other?
3. 


------------------------------------ **Differences to Know:** ---------------------------------------------

1. Difference b/w Replica Controller and Replicaset
2. Difference b/w Replicaset and deployment
3. Differences b/w deployment and statefullset
4. Difference b/w Replicaset and deployment
5. Difference b/w Liveness Probe and Readiness Probe ? ---> and Check on Startup Probe.

