# Cloud-Native-Podcast

##  Title: Kubernetes Operators A Definitive Guide for Platform Engineers - [Episode 83](https://youtube.com/live/P77ku0sMIfQ)

## Speakers Intro:
Welcome [Rose Crisp](https://www.linkedin.com/in/manna-kong/) to the [show](https://twitter.com/cloudnativefm/status/1679480605619421186) with over 15 years of software engineering experience. She will be joining us on the [cloud-native podcast](https://www.youtube.com/@cloudnativefm). She has become captivated by the immense possibilities of Kubernetes as a passionate advocate for Kubernetes operators and a member of the Red Hat team. She actively contributes to the open-source community shaping the future of Kubernetes. 

#### Speakers Blogs [Operator 101](https://github.com/rocrisp/blogs/blob/main/Operator101.md) [inner workings of the l5-operator](https://github.com/rocrisp/blogs/blob/main/l5-operator.md#Introducing-l5-operator)

### Description:
K8s Operators are software extensions that make use of Kubernetes APIs to extend behavior. What do we need to know about how they work, and what are the concrete benefits? Tune into real-world use cases where operators and CRDs have been instrumental in solving complex application deployment and management challenges. Moreover how operators enable automation, scalability, and self-healing in various scenarios.

### Understanding Kubernetes Operators:
Kubernetes Operators are a set of custom controllers that extend the capabilities of Kubernetes by automating the management of complex applications or services. They embody operational knowledge and domain-specific expertise, allowing Kubernetes to handle workloads beyond simple container orchestration. Operators enable users to declare the desired state of an application, and the Operator actively works to ensure the actual state aligns with the declared state, ensuring continuous reconciliation.

### CRD concepts in K8S
To begin to understand what CRD is, we must go over a couple of concepts in Kubernetes:

-  A resource is an endpoint in k8s API that allows you to store an API object of any kind.
-  A custom resource allows you to create your own API objects and define your own kind just like Pod, Deployment, ReplicaSet, etc.

CRDs allow users to create new types of resources without adding another API server. You do not need to understand API Aggregation to use CRDs. Regardless of how they are installed, the new resources are referred to as Custom Resources to distinguish them from built-in Kubernetes resources (like pods). This concept of CRD is introduced in Kubernetes 1.7, this is useful when we want to add our own created object inside the Kubernetes cluster to full fill or meet the requirement. 

###  Why Do We Need Kubernetes Operators?

-  **Automation and Autonomy:** Operators automate repetitive tasks, freeing developers and operators from manual intervention, thereby increasing efficiency and autonomy.

-  **Stateful Application Management:** Operators excel at managing stateful applications, such as databases, queues, and storage systems, which require more complex lifecycle operations.

-  **Self-Healing and Resilience:** Operators monitor the health of applications and services, automatically triggering recovery actions in case of failures, promoting self-healing and enhanced resilience.

-  **Simplified Scaling:** Operators facilitate horizontal and vertical scaling based on resource demands, dynamically adjusting the application's capacity as needed.

-  **Upgrades and Updates:** Operators manage the seamless upgrade and update process, ensuring minimal downtime and disruptions during version changes.

-  **Configuration Management:** Operators handle the configuration of applications, simplifying the process of applying changes and maintaining consistency.

###  How to Write a Kubernetes Operator from Scratch:

-  **Define the Custom Resource Definition (CRD):** Begin by defining the CRD that represents the custom resource managed by the Operator. This CRD encapsulates the desired state and parameters of the application.

-  **Create the Controller:** Implement the custom controller that reconciles the declared state with the actual state of the application. The controller watches for changes in the CRD and takes appropriate actions to ensure alignment.

-  **Implement the Reconciliation Logic:** The reconciliation logic defines how the Operator brings the application to its desired state. This includes provisioning, scaling, configuration management, and self-healing mechanisms.

-  **Handle Events and Watchers:** Set up event watchers to monitor changes in the Kubernetes API. Use these events to trigger the reconciliation process and respond to state changes.

-  **Testing and Debugging:** Thoroughly test the Operator's functionality, ensuring it responds correctly to various scenarios and edge cases. Debug any issues and iteratively refine the implementation.

-  **Deployment and Versioning:** Package the Operator as a Kubernetes-native application, deploy it, and manage its lifecycle using Kubernetes mechanisms.

#### Learning resources - Videos
-  [Writing a Kubernetes Operator from Scratch Using Kubebuilder - Dinesh Majrekar](https://www.youtube.com/watch?v=LLVoyXjYlYM)
-  [Tutorial: Becoming a Kubernetes Developer: Writing Your First Operator - Abby Bangser, Syntasso](https://www.youtube.com/watch?v=fDkoxrz7BXw)
-  [Creating a Go Operator from scratch with Jay Dobies and Chris Short](https://www.youtube.com/watch?v=Uu9fwiJBckw)
-  [Unlocking the power of Kubernetes: Create your own resources with CRDs | PlatformCon 2023](https://www.youtube.com/watch?v=B4EF52zY6EM)
-  [Kubernetes Operator simply explained in 10 mins](https://www.youtube.com/watch?v=ha3LjlD6g7g)
-  [Let's build a Kubernetes Operator in Go! with Michael Gasch & Rafael Brito](https://www.youtube.com/watch?v=8Ex7ybi273g)

#### Articles:
-  [Build a Kubernetes Operator in six steps](https://developers.redhat.com/articles/2021/09/07/build-kubernetes-operator-six-steps#)
-  [Ultimate Guide to Kubernetes Operators and How to Create New Operators](https://komodor.com/learn/kubernetes-operator/)
-  [Exploring Kubernetes Operator Patterns](https://iximiuz.com/en/posts/kubernetes-operator-pattern/)
-  [What is a CRD (Custom Resource Definition) ?](https://www.wallarm.com/what/what-is-a-crd-custom-resource-definition)
-  [Kubernetes CRDs: What They Are and Why They Are Useful](https://thenewstack.io/kubernetes-crds-what-they-are-and-why-they-are-useful/)
-  [Extending Kubernetes APIs with Custom Resource Definitions (CRDs)](https://medium.com/velotio-perspectives/extending-kubernetes-apis-with-custom-resource-definitions-crds-139c99ed3477)

#### Course:
-  [Writing Kubernetes Operator (Kluster) from Scratch](https://www.infracloud.io/kubernetes-school/writing-k8s-operator-kluster/)
-  [Kubernetes Operators | Udemy](https://www.udemy.com/course/kubernetes-operators/)

#### Kubernetes Docs:
-  [Operators](https://kubernetes.io/docs/concepts/extend-kubernetes/operator/) are software extensions to Kubernetes that make use of [custom resources](https://kubernetes.io/docs/concepts/extend-kubernetes/api-extension/custom-resources/) to manage applications and their components.

#### Community:
-  [OperatorHub.io](https://operatorhub.io/) is a new home for the Kubernetes community to share Operators.
### 👋 Contact me 👋 
-   https://twitter.com/cloudnativeboy
-   https://www.linkedin.com/in/saim-safder/ 

