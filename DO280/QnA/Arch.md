# Architecture of OpenShift

### 1. Which of the following definitions best describes container orchestration platforms?
a. They extend your application's operational knowledge and provide a way to package and distribute them. \
b. **They allow you to manage a cluster of servers that run containerized applications. They add features such as self-service, high availability, monitoring, and automation.** \
c. They allow you to provision Infrastructure-as-a-Service clusters on a variety of cloud providers, including AWS, GCP, and Microsoft Azure. \
d. They enable developers to write, package, and publish their applications as operators to the operator catalog.

### 2. Which three of the following key features enable high availability for your applications?
(Choose three.) \
a. An OpenShift etcd cluster keeps the cluster state available for all nodes. \
b. **OpenShift HAProxy load balancers allow external access to applications.** \
c. **OpenShift services load balance access to applications from inside the cluster.** \
d. **OpenShift deployment configurations ensure application containers are restarted in scenarios such as loss of a node.**

## 3. Which two of the following statements about OpenShift are true? \ 
(Choose two.) \
a. () Developers can create and start cloud applications directly from a source code repository. \
b. OpenShift patches Kubernetes to add features that would not be available to other distributions of Kubernetes. \
c. OpenShift Dedicated gives you access to an exclusive set of operators that Red Hat curates and maintains. This helps to ensure that the operators are secure and safe to run in your environment. \
d. **OpenShift cluster administrators can discover and install new operators from the operator catalog.**

### 4. Which two of the following services do OpenShift components use for load balancing their traffic? 
(Choose two.) \
a. The OpenShift API, which is accessible over the external load balancer. \
b. **Services, which use Netfilter for load balancing.** \
c. Services, which use HAProxy for load balancing. \ 
d. Routes, which use Netfilter for load balancing. \
e. **Routes, which use the HAProxy for load balancing.** \

### 5. Which two of the following statements about OpenShift high availability and scaling are true? 
(Choose two.) \
a. OpenShift does not provide high availability by default. You need to use third-party high availability products.
b. **OpenShift uses metrics from Prometheus to dynamically scale application pods.**
c. High availability and scaling are restricted to applications that expose a REST API.
d. **OpenShift can scale applications up and down based on demand.**


**1. OpenShift is based on which of the following container orchestration technologies?** 
   a. Docker Swarm \
   b. Rancher \
   **c. Kubernetes** \
   d. Mesosphere Marathon \
   e. CoreOS Fleet \

### 2. Which two of the following statements are true of OpenShift Container Platform?
(Choose two.)\
a. **OpenShift provides an OAuth server that authenticates calls to its REST API.** \
b. **OpenShift requires the CRI-O container engine.** \
c. Kubernetes follows a declarative architecture, but OpenShift follows a more traditional imperative architecture. \
d. OpenShift extension APIs run as system services.

### 3. Which of the following servers runs Kubernetes API components? \
a. Worker nodes \
b. Nodes \
c. **Control plane nodes** \

### 4. Which of the following components does OpenShift add to upstream Kubernetes? 
a. The etcd database \
b. A container engine \
c. **A registry server** \
d. A scheduler \
e. The Kubelet \

### 5. Which of the following sentences is true regarding support for storage with OpenShift? 
a. Users can only store persistent data in the etcd database. \
b. Users can only deploy on OpenShift cloud-native applications that conform to the Twelve-Factor App methodology. \
c. Administrators must configure storage plug-ins appropriate for their cloud providers. \
d. Administrators must define persistent volumes before any user can deploy applications that require persistent storage. \
e. **Users can deploy applications that require persistent storage by relying on the default storage class.** 


