
# Hosting applications on Azure

Azure provides a variety of different ways to host your application depending on your needs.

The services you choose will often come down to two considerations:

- Do you prefer simplicity or control?
- Do you prefer cloud-native (i.e., containers) or Azure-native (tailored tools and integrations)
## Simplicity and control

Azure hosting services are provided with two considerations:- 

- **Simplicity versus control**
    - Simple hosting platforms require less configuration and management but provide less control over the underlying infrastructure.
    - More complex hosting platforms require more configuration and management but provide more control over the underlying infrastructure.
    
- **Cloud-native versus Azure-native**
	-  Cloud-native can be thought of as cloud-portable using open-source workloads such as containers and open-source technologies such as Dapr. The applications you build can be deployed to any cloud provider.
	- Azure-native is specific to Azure with an investment in Azure-specific tools and technologies to manage that infrastructure
## Simplified hosting

**Simplified** hosting solutions are fully managed by Azure. You're responsible for the functionality such as code and environment configuration.
- [Logic Apps](https://learn.microsoft.com/en-us/azure/logic-apps/logic-apps-overview): Create and run automated workflows with little to no code.
- [Power Automate](https://learn.microsoft.com/en-us/power-automate): Use when you need to automate business processes and workflows.
- [Azure Static Web Apps](https://learn.microsoft.com/en-us/azure/static-web-apps): Deploy generated static web apps such as Blazor and React.
- [Azure Functions Apps](https://learn.microsoft.com/en-us/azure/azure-functions): serverless code or container hosting.

## Balanced hosting
**Balanced** hosting solutions balance the need for simplicity with the need for control. You're responsible for the functionality such as code and environment configuration. Azure manages the underlying runtime and infrastructure including updates and patches. You can also bring your own container to the service. Balanced hosting is both Azure-native and Cloud-native.

- [Azure App Service](https://learn.microsoft.com/en-us/azure/app-service): Full-service web hosting including language runtimes, containers, and automation workloads.
- [Azure Container Apps](https://learn.microsoft.com/en-us/azure/container-apps): Serverless container hosting.
- [Azure Spring Apps](https://learn.microsoft.com/en-us/azure/spring-apps): Migrate Spring Boot applications to the Azure cloud.

## Controlled hosting

**Controlled** hosting solutions give you full control over the underlying infrastructure. You're responsible for updates and patches as well as your code, assets, and environment configuration. Controlled hosting is the cloud-native approach.

- [Azure Virtual Machines](https://learn.microsoft.com/en-us/azure/virtual-machines): Full control of VM.
- [Azure Kubernetes Service](https://learn.microsoft.com/en-us/azure/aks): Full control of Kubernetes cluster.


## Source-code hosting

- ![[Pasted image 20250218104127.png]]

### No code or low code

Azure supports no-code solutions are part of its Azure-Cloud approach.

- [Logic Apps](https://learn.microsoft.com/en-us/azure/logic-apps/logic-apps-overview): Use a visual designer with prebuilt operations to develop a workflow for your enterprise and business-to-business scenarios.
- [Power Automate](https://learn.microsoft.com/en-us/power-automate) such as [Power apps](https://learn.microsoft.com/en-us/power-apps): Use when you need to automate business processes and workflows within the Microsoft 365 organization.

### Code vs container

**Low-code** hosting solutions are designed to allow you to bring your code functionality without having to manage the application infrastructure.

- [Azure Static Web Apps](https://learn.microsoft.com/en-us/azure/static-web-apps): deploy generated static web apps.
- [Azure Functions](https://learn.microsoft.com/en-us/azure/azure-functions): deploy code functions in supported languages without having to manage the application infrastructure.
**Code-first** hosting solutions are designed to host code. You can deploy your code directly to the hosting solution.

- [Azure App Service](https://learn.microsoft.com/en-us/azure/app-service): full-service web hosting.
- [Azure Spring Apps](https://learn.microsoft.com/en-us/azure/spring-apps): Spring Boot applications.

**Container-first** hosting solutions are designed to host containers. The service provides container-specific configuration options and features. You're responsible for the compute used inside the container. The services which host containers move from managed control to full responsibility so you only take on the amount of container management you want.

**Kubernetes-centric** orchestration hosting includes:

| Service                                                                        | Focus        | Use                                                                                                                                                                                                                                                                                          |     |     |
| ------------------------------------------------------------------------------ | ------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --- | --- |
| [Azure Kubernetes Service](https://learn.microsoft.com/en-us/azure/aks)        | Cloud-native | Use for Kubernetes clusters with a **declarative** approach using configuration files and external artifacts.                                                                                                                                                                                |     |     |
| [Azure Service Fabric](https://learn.microsoft.com/en-us/azure/service-fabric) | Azure-native | Use an **imperative** approach to deploying microservices across clusters of machines. It provides a programming model that allows developers to write code that describes the desired state of the system, and the Service Fabric runtime takes care of making the system match that state. |     |     |
|                                                                                |              |                                                                                                                                                                                                                                                                                              |     |     |

## Most Popular Hosting Options :-


### **1. Azure App Service (Web Apps)**

A fully managed Platform-as-a-Service (PaaS) for hosting web applications, RESTful APIs, and mobile backends.

✅ **Benefits:**

- Fully managed, handles scaling, security, and patching
- Supports multiple programming languages (Python, .NET, Java, PHP, etc.)
- Integrated CI/CD with GitHub, Azure DevOps
- Built-in autoscaling and load balancing

❌ **Drawbacks:**

- Limited customization compared to IaaS (VMs)
- Costs can increase with high-scale apps
- Less control over the underlying infrastructure

🔹 **Best Use Case:**  
Ideal for hosting web apps, APIs, and microservices without worrying about infrastructure management.

📌 **Example:**  
Hosting an e-commerce website built with .NET on Azure App Service.

---

### **2. Azure Virtual Machines (IaaS)**

Provides full control over the operating system, runtime, and application environment.

✅ **Benefits:**

- Full control over OS, security, and network configuration
- Can run any application that requires a traditional server environment
- Scales manually or with Azure Scale Sets

❌ **Drawbacks:**

- Requires management of OS updates, security patches, and scaling
- Higher operational complexity compared to PaaS solutions

🔹 **Best Use Case:**  
Ideal for hosting applications that require custom configurations, legacy applications, or software requiring full control over the environment.

📌 **Example:**  
Hosting a legacy .NET Framework application on a Windows Server VM.

---

### **3. Azure Kubernetes Service (AKS)**

A managed Kubernetes service for containerized applications.

✅ **Benefits:**

- Automated cluster management and scaling
- Supports microservices and containerized applications
- Integrated monitoring and security features

❌ **Drawbacks:**

- Steeper learning curve for Kubernetes management
- Requires proper configuration for networking and security

🔹 **Best Use Case:**  
Best for hosting microservices architectures and applications requiring orchestration.

📌 **Example:**  
Deploying a multi-container application with microservices using AKS.

---

### **4. Azure Functions (Serverless)**

A serverless compute option for running event-driven code without managing infrastructure.

✅ **Benefits:**

- Auto-scales based on demand
- Pay-per-execution pricing model reduces costs
- No need to manage servers

❌ **Drawbacks:**

- Execution time limits (default 5 minutes, extendable)
- Cold start latency for infrequent executions

🔹 **Best Use Case:**  
Best for event-driven applications like background processing, real-time data processing, and automation.

📌 **Example:**  
Processing new orders and sending confirmation emails using an Azure Function.

---

### **5. Azure Container Apps**

A fully managed serverless container platform.

✅ **Benefits:**

- Simplifies container deployment without managing Kubernetes
- Built-in autoscaling with KEDA (Kubernetes-based Event-Driven Autoscaling)
- Supports microservices patterns

❌ **Drawbacks:**

- Less customization than AKS
- Not suitable for complex containerized applications requiring full Kubernetes features

🔹 **Best Use Case:**  
Best for deploying microservices, API backends, and lightweight containerized apps.

📌 **Example:**  
Hosting a containerized Node.js API without managing Kubernetes clusters.

---

### **6. Azure Service Fabric**

A distributed systems platform for building scalable and reliable microservices applications.

✅ **Benefits:**

- Supports both containers and traditional microservices
- High reliability and self-healing features
- Can run on Azure or on-premises

❌ **Drawbacks:**

- Higher complexity compared to AKS
- Requires deeper knowledge of Service Fabric APIs

🔹 **Best Use Case:**  
Best for high-scale, enterprise-grade applications requiring stateful services.

📌 **Example:**  
Hosting a banking application that requires distributed microservices.

---

### **7. Azure Spring Apps**

A fully managed PaaS for Spring Boot applications.

✅ **Benefits:**

- Optimized for Spring Boot apps
- Integrated scaling, monitoring, and security
- Reduces operational overhead for Java applications

❌ **Drawbacks:**

- Only suitable for Spring Boot-based applications
- Costs may be higher than self-managed options

🔹 **Best Use Case:**  
Ideal for Java developers using Spring Boot to build cloud-native applications.

📌 **Example:**  
Deploying a Spring Boot e-commerce application with auto-scaling.

---

### **8. Azure Static Web Apps**

A service for hosting static front-end applications with automatic integration with APIs.

✅ **Benefits:**

- Free or low-cost hosting for static sites
- Built-in CI/CD integration with GitHub Actions
- Serverless API integration with Azure Functions

❌ **Drawbacks:**

- Limited to static content + APIs
- Not suitable for server-side rendered (SSR) applications

🔹 **Best Use Case:**  
Perfect for hosting static websites, personal blogs, and single-page applications (SPAs).

📌 **Example:**  
Hosting a React or Angular SPA with a serverless backend.

---

### **9. Azure Red Hat OpenShift**

A managed OpenShift Kubernetes service.

✅ **Benefits:**

- Provides OpenShift’s enterprise Kubernetes capabilities
- Fully managed with integrated security
- Supports hybrid cloud deployments

❌ **Drawbacks:**

- Higher cost compared to AKS
- Requires OpenShift expertise

🔹 **Best Use Case:**  
Best for organizations already using OpenShift for containerized workloads.

📌 **Example:**  
Running enterprise applications requiring OpenShift’s advanced capabilities.

---

### **10. Azure Batch**

A service for large-scale parallel and high-performance computing (HPC).

✅ **Benefits:**

- Supports large-scale parallel processing
- Cost-effective as resources are allocated dynamically
- Integrates with Azure HPC environments

❌ **Drawbacks:**

- Not suitable for web apps or APIs
- Requires proper workload scheduling

🔹 **Best Use Case:**  
Best for scientific computing, data analysis, and batch processing.

📌 **Example:**  
Processing large-scale simulations in the healthcare or finance industry.