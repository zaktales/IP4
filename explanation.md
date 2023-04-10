# Deploy microservices on Kubernetes

Kubernetes (k8s) has gained widespread adoption as a platform for microservices due to its ability to seamlessly automate app deployment at scale.

Kubernetes touts itself as “a portable, extensible open-source platform for managing containerized workloads and services”. In simple terms, Kubernetes helps to automate the deployment and management of containerized applications. This means we can package an app (code, dependencies and config) in a container and hand it over to Kubernetes to deploy and scale without worrying about our infrastructure. Under the hood, Kubernetes decides where to run what, monitors the systems and fixes things if something goes wrong.

## Microservice architecture

According to [James Lewis’ and Martin Fowler’s definition of microservices](https://martinfowler.com/microservices/) we can see why Kubernetes is such a good solution for the architecture. “The microservice architectural style is an approach to developing a single application as a suite of small services, each running in its own process and communicating with lightweight mechanisms, often an HTTP resource API. These services are built around business capabilities and independently deployable by **fully automated deployment machinery**. There is a bare minimum of centralized management of these services, which may be written in different programming languages and use different data storage technologies”. Kubernetes is in fact a “fully automated deployment machine” that provides a powerful abstraction layer atop server infrastructure.

## Common Kubernetes terms

Below are some common terms associated with Kubernetes.

- **Node**: A node is a single machine in a Kubernetes cluster. It can be a virtual or physical machine.
- **Cluster**: A cluster consists of at least one master machine and multiple worker machines called nodes.
- **Pod**: A pod is the basic unit of computing in Kubernetes. Containers are not run directly. Instead, they are wrapped in a pod.
- **Deployment**: A deployment is used to manage a pod or set of pods. Pods are typically not created or managed directly. Deployments can automatically spin up any number of pods. If a pod dies, a deployment can automatically recreate it as well.
- **Service**: Pods are mortal. Consumers should however not be burdened with figuring out what pods are available and how to access them. Services keep track of all available pods of a certain type and provide a way to access them.
