---
marp: true
theme: default
class:
  - lead
paginate: true
backgroundColor: #89f0a5
---

# **Azure Fundamentals Course Jan 2026**

**Piti Champeethong (Fyi/ฟี่)**
**LinkedIn: [pitichampeethong](https://www.linkedin.com/in/pitichampeethong/)**
**Date: 07 - 08 Jan 2026**

---

## **Agenda**

* **Part 1: Introduction to Cloud Concepts**
  * Module 1: Cloud Concepts
* **Part 2: Azure Architecture and Services**
  * Module 2: Azure Architecture
  * Module 3: Core Azure Services
  * Lab 1
  * Module 4: Azure Solutions

---

## **Agenda (Continue)**

* **Part 3: Azure Management and Governance**
  * Module 5: Azure Management Tools
  * Module 6: Security
  * Lab 2
  * Module 7: Governance and Compliance
* **Part 4: Conclusion and Workshops**

---

## **What is Cloud Computing?**

A model for enabling ubiquitous, convenient, on-demand network access to a shared pool of configurable computing resources (e.g., networks, servers, storage, applications, and services) that can be rapidly provisioned and released with minimal management effort or service provider interaction.

**In simple terms: It's about renting resources, like compute power and storage, from someone else's data center.**

---

## **Why Cloud Computing?**

* **Cost-Effective:** Pay only for what you use (Pay-as-you-go).
* **Scalable:** Scale up or down as your needs change.
* **Elastic:** Automatically scale based on demand.
* **Always On:** High availability and fault tolerance.
* **Global:** Deploy applications closer to your users.
* **Fast:** Quickly provision resources.

---

## **Module 1: Cloud Concepts**

* High-Level Overview of Cloud Concepts
* Cloud Models: IaaS, PaaS, SaaS
* Cloud Deployment Models: Public, Private, Hybrid
* CapEx vs OpEx
* Benefits of Cloud Computing

---

## **Cloud Models: IaaS, PaaS, SaaS**

A way to categorize the services that cloud providers offer.

* **IaaS:** Infrastructure as a Service
* **PaaS:** Platform as a Service
* **SaaS:** Software as a Service

[Cloud Models Image](images/cloud_model.png)

---

## **IaaS: Infrastructure as a Service**

* The most basic category of cloud computing services.
* You rent IT infrastructure—servers and virtual machines (VMs), storage, networks, operating systems—from a cloud provider on a pay-as-you-go basis.
* **You manage:** Applications, Data, Runtime, Middleware, OS
* **Provider manages:** Virtualization, Servers, Storage, Networking

**Example:** Azure Virtual Machines

---

## **PaaS: Platform as a Service**

* Provides a platform for customers to develop, run, and manage applications without the complexity of building and maintaining the infrastructure.
* **You manage:** Applications, Data
* **Provider manages:** Runtime, Middleware, OS, Virtualization, Servers, Storage, Networking

**Example:** Azure App Service

---

## **SaaS: Software as a Service**

* Provides a complete software product that is run and managed by the service provider.
* You just use the software, usually through a web browser.
* **You manage:** Nothing
* **Provider manages:** Everything

**Example:** Microsoft 365, Gmail

---

## **Cloud Deployment Models**

* **Public Cloud:** Owned and operated by a third-party cloud service provider.
* **Private Cloud:** Used exclusively by a single business or organization.
* **Hybrid Cloud:** Combines public and private clouds.

---

## **Public Cloud**

* Resources are owned and operated by a third-party cloud service provider and delivered over the Internet.
* **Benefits:** Lower costs, no maintenance, near-unlimited scalability, high reliability.
* **Drawbacks:** Less control, potential security and compliance concerns.

**Example:** Microsoft Azure, Amazon Web Services (AWS), Google Cloud Platform (GCP)

---

## **Private Cloud**

* Computing resources are used exclusively by a single business or organization.
* The private cloud can be physically located on the company’s on-site data center, or it can be hosted by a third-party service provider.
* **Benefits:** More control, improved security and privacy.
* **Drawbacks:** Higher costs, more maintenance.

---

## **Hybrid Cloud**

* Combines public and private clouds, allowing data and applications to be shared between them.
* **Benefits:** Flexibility, scalability, security.
* **Drawbacks:** More complex to manage.

---

## **CapEx vs OpEx**

* **CapEx (Capital Expenditure):** Spending money on physical infrastructure up front, and then deducting that expense from your tax bill over time.
* **OpEx (Operational Expenditure):** Spending money on services or products now and being billed for them now. There's no upfront cost.

Cloud computing shifts IT spending from CapEx to OpEx.

---

## **Benefits of Cloud Computing**

* **Scalability:** The ability to increase or decrease resources as needed.
* **Elasticity:** The ability to automatically or dynamically increase or decrease resources as needed.
* **Agility:** The ability to react quickly to changing business needs.

---

## **Benefits of Cloud Computing (Continue)**

* **High Availability:** The ability of a system to be continuously operational for a long period of time.
* **Fault Tolerance:** The ability of a system to continue to function in the event of a failure of some of its components.
* **Disaster Recovery:** The ability to recover from a disaster and continue to function.

---

## **Consumption-based model**

* Pay for what you use.
* No upfront costs.
* Stop paying for resources when you no longer need them.

---

## **Module 1 Summary**

* Cloud Computing is renting resources from someone else's data center.
* Cloud Models: IaaS, PaaS, SaaS.
* Cloud Deployment Models: Public, Private, Hybrid.
* Cloud computing is an OpEx model.
* Benefits: Scalability, Elasticity, Agility, High Availability, Fault Tolerance, Disaster Recovery.

---

## **Q&A for Part 1**

Any questions about the introduction to cloud concepts?

---
---

## **Module 2: Azure Architecture**

* Azure Global Infrastructure
* Azure Resources and Resource Groups
* Subscriptions and Management Groups
* Azure Resource Manager (ARM)

---

## **Azure Global Infrastructure**

Azure is made up of a massive global network of datacenters.

* **Regions:** A geographic area on the planet containing at least one, but potentially multiple datacenters that are nearby and networked together with a low-latency network.
* **Availability Zones:** Physically separate datacenters within a single region.

[Azure Regions](https://datacenters.microsoft.com/globe/explore)

---

## **Azure Regions**

* Azure has more global regions than any other cloud provider.
* This gives you the flexibility to deploy applications where you need to.
* Some services are only available in certain regions.

---

## **Availability Zones**

* Each Availability Zone is an isolated boundary.
* If one zone goes down, the other continues to work.
* Provide high availability for your applications.
* Not all regions have Availability Zones.

---

## **Region Pairs**

* Each Azure region is paired with another region within the same geography.
* This allows for the replication of resources across a geography that helps reduce the likelihood of interruptions.
* Example: West US is paired with East US.

---

## **Azure Resources and Resource Groups**

* **Resource:** A manageable item that is available through Azure. Examples: Virtual machines, storage accounts, web apps, databases, and virtual networks.
* **Resource Group:** A container that holds related resources for an Azure solution.

---

## **Subscriptions and Management Groups**

* **Subscription:** A logical container for your resources. It's also a billing unit.
* **Management Group:** A container for managing access, policy, and compliance across multiple Azure subscriptions.

---

## **Azure Resource Manager (ARM)**

* The deployment and management service for Azure.
* Provides a management layer that enables you to create, update, and delete resources in your Azure account.
* You can use ARM to manage your infrastructure through a declarative template rather than scripts.

---

## **ARM Templates**

* A JavaScript Object Notation (JSON) file that defines one or more resources to deploy to a resource group, subscription, management group, or tenant.
* Allows you to implement infrastructure as code for your Azure solutions.

---

## **Module 2 Summary**

* Azure has a global infrastructure of regions and availability zones.
* Resources are the manageable items in Azure.
* Resource groups are containers for resources.
* Subscriptions are billing units and containers for resources.
* Management groups are for managing multiple subscriptions.
* ARM is the deployment and management service for Azure.

---

## **Module 3: Core Azure Services**

* Compute Services
* Networking Services
* Storage Services
* Database Services

---

## **Compute Services: Virtual Machines (VMs)**

* The most basic compute service in Azure.
* You can create a VM with a specific OS, CPU, RAM, and storage.
* You are responsible for managing the OS and the software on the VM.

---

## **VM Scale Sets**

* Create and manage a group of load-balanced VMs.
* The number of VM instances can automatically increase or decrease in response to demand or a defined schedule.

---

## **App Service**

* A PaaS offering that enables you to build and host web apps, mobile backends, and RESTful APIs in the programming language of your choice without managing infrastructure.
* Supports Windows and Linux.

---

## **Azure Functions (Serverless)**

* A serverless compute service that lets you run event-triggered code without having to explicitly provision or manage infrastructure.
* Pay only for the time your code is running.

---

## **ACI and AKS**

* **Azure Container Instances (ACI):** A serverless container runtime that allows you to run containers without managing the underlying infrastructure.
* **Azure Kubernetes Service (AKS):** A managed container orchestration service based on the open-source Kubernetes system.

---

## **Networking Services: Virtual Network (VNet)**

* A virtual network that enables Azure resources like VMs to securely communicate with each other, the internet, and on-premises networks.
* A VNet is scoped to a single region.

---

## **Subnets and Network Security Groups (NSGs)**

* **Subnet:** A range of IP addresses in the VNet. You can launch Azure resources into a subnet.
* **Network Security Group (NSG):** A firewall that contains a list of security rules that allow or deny network traffic to resources connected to Azure VNets.

---

## **Azure DNS**

* A hosting service for DNS domains that provides name resolution by using Microsoft Azure infrastructure.
* You can host your DNS domains in Azure.

---

## **VPN Gateway and ExpressRoute**

* **VPN Gateway:** A service that sends encrypted traffic between an Azure virtual network and an on-premises location over the public Internet.
* **ExpressRoute:** A private connection between your on-premises network and Azure.

---

## **Storage Services: Blob Storage**

* Object storage for unstructured data.
* Store and access large amounts of unstructured data, such as text or binary data.

---

## **Disk Storage**

* Provides disks for Azure virtual machines.
* Two types: Standard (HDD) and Premium (SSD).

---

## **File Storage**

* A managed file share service that you can access via the Server Message Block (SMB) protocol.
* Mount file shares in the cloud or on-premises.

---

## **Storage Tiers**

* **Hot:** Optimized for storing data that is accessed frequently.
* **Cool:** Optimized for storing data that is infrequently accessed and stored for at least 30 days.
* **Archive:** Optimized for storing data that is rarely accessed and stored for at least 180 days with flexible latency requirements.

---

## **Database Services: Cosmos DB**

* A globally distributed, multi-model database service.
* Supports NoSQL databases.
* Offers turnkey global distribution.

---

## **Azure SQL Database**

* A fully managed relational database service based on the latest stable version of the Microsoft SQL Server database engine.
* A PaaS service.

---

## **Azure Database for MySQL/PostgreSQL/MariaDB**

* Fully managed, enterprise-ready community database as a service.
* PaaS offerings.

---

## **Azure Synapse Analytics**

* An analytics service that brings together enterprise data warehousing and Big Data analytics.
* Query data on your terms, using either serverless or provisioned resources at scale.

---

## **Module 3 Summary**

* **Compute:** VMs, Scale Sets, App Service, Functions, ACI, AKS
* **Networking:** VNet, Subnets, NSGs, DNS, VPN Gateway, ExpressRoute
* **Storage:** Blob, Disk, File Storage
* **Databases:** Cosmos DB, SQL Database, MySQL/PostgreSQL/MariaDB, Synapse

---

## **Lab 1: Objectives**

* Create a Virtual Machine in the Azure Portal.
* Create a Storage Account in the Azure Portal.

---

## **Lab 1: Instructions - Create a VM**

1. Go to the Azure Portal.
2. Click on "Create a resource".
3. Search for "Virtual machine".
4. Click "Create".
5. Fill in the required details:
    * Subscription, Resource Group
    * Virtual machine name
    * Region, Image
    * Size, Administrator account
    * Inbound port rules
6. Click "Review + create" and then "Create".

---

## **Lab 1: Instructions - Create a Storage Account**

1. Go to the Azure Portal.
2. Click on "Create a resource".
3. Search for "Storage account".
4. Click "Create".
5. Fill in the required details:
    * Subscription, Resource Group
    * Storage account name
    * Region, Performance
    * Redundancy
6. Click "Review + create" and then "Create".

---

## **Lab 1: Review and Q&A**

* What did we do in this lab?
* Any questions?

---

## **Lab 1: Completed**

You have successfully created a VM and a Storage Account.

---

## **Module 4: Azure Solutions**

* Azure IoT Hub
* Azure Big Data and Analytics
* Azure AI and Machine Learning
* Azure Serverless Computing

---

## **Azure IoT Hub**

* A managed service that acts as a central message hub for bi-directional communication between your IoT application and the a device it manages.
* Connect, monitor, and manage billions of IoT assets.

---

## **Azure Big Data and Analytics**

* A collection of services to help you with big data.
* **Azure Synapse Analytics:** Analytics service that brings together enterprise data warehousing and Big Data analytics.
* **Azure HDInsight:** A managed, full-spectrum, open-source analytics service for enterprises.
* **Azure Databricks:** A fast, easy, and collaborative Apache Spark-based analytics platform.

---

## **Azure AI and Machine Learning**

* A range of services that you can use to build and deploy AI and machine learning models.
* **Azure Machine Learning:** A cloud service for training, deploying, and managing machine learning models.
* **Cognitive Services:** A comprehensive family of AI services and cognitive APIs to help you build intelligent apps.

---

## **Azure Serverless Computing**

* Abstracts the servers you run on.
* You don't have to worry about the infrastructure.
* **Azure Functions:** Run event-triggered code.
* **Logic Apps:** Automate workflows.
* **Event Grid:** A fully-managed event routing service.

---

## **Module 4 Summary**

* **IoT:** IoT Hub
* **Big Data:** Synapse, HDInsight, Databricks
* **AI/ML:** Azure Machine Learning, Cognitive Services
* **Serverless:** Functions, Logic Apps, Event Grid

---
---

## **Module 5: Azure Management Tools**

* Azure Portal
* Azure Cloud Shell
* Azure CLI
* Azure PowerShell
* Azure Mobile App
* Azure Advisor
* Azure Monitor
* Azure Service Health

---

## **Azure Portal**

* A web-based, unified console that provides an alternative to command-line tools.
* With the Azure portal, you can manage your Azure subscription using a graphical user interface.
* You can build, manage, and monitor everything from simple web apps to complex cloud deployments.

---

## **Azure Cloud Shell**

* An interactive, authenticated, browser-accessible shell for managing Azure resources.
* It provides the flexibility of choosing the shell experience that best suits the way you work, either Bash or PowerShell.

---

## **Azure CLI**

* A cross-platform command-line program that connects to Azure and executes administrative commands on Azure resources.
* It can be used to create, manage, and delete Azure resources from the command line.

---

## **Azure PowerShell**

* A set of cmdlets for managing Azure resources directly from the PowerShell command line.
* Azure PowerShell is designed to make it easy to learn and get started with, but provides powerful features for automation.

---

## **Azure Mobile App**

* Stay connected to your Azure resources—anytime, anywhere.
* Check the status and important metrics of your services.
* Get notifications and alerts about important health issues.
* Run commands to manage your resources.

---

## **Azure Advisor**

* A personalized cloud consultant that helps you follow best practices to optimize your Azure deployments.
* It analyzes your resource configuration and usage telemetry and then recommends solutions that can help you improve the cost effectiveness, performance, high availability, and security of your Azure resources.

---

## **Azure Monitor**

* A comprehensive solution for collecting, analyzing, and acting on telemetry from your cloud and on-premises environments.
* It helps you understand how your applications are performing and proactively identifies issues affecting them and the resources they depend on.

---

## **Azure Service Health**

* Provides personalized guidance and support when issues in Azure services affect you.
* It can notify you, help you understand the impact of issues, and keep you updated as the issue is resolved.

---

## **Module 5 Summary**

* **Management Tools:** Portal, Cloud Shell, CLI, PowerShell, Mobile App
* **Monitoring and Optimization:** Advisor, Monitor, Service Health

---

## **Module 6: Security**

* Shared Responsibility Model
* Azure Security Center
* Azure Active Directory (Azure AD)
* Multi-Factor Authentication (MFA)
* Network Security
* Key Vault

---

## **Shared Responsibility Model**

* Describes the responsibilities between the cloud provider (Microsoft) and you (the customer).
* The responsibilities vary depending on the cloud service model (IaaS, PaaS, SaaS).

[Shared Responsibility Model](images/cloud_model.png)

---

## **Azure Security Center**

* A unified infrastructure security management system that strengthens the security posture of your data centers.
* Provides threat protection across your hybrid workloads in the cloud and on-premises.

---

## **Azure Active Directory (Azure AD)**

* Microsoft’s cloud-based identity and access management service.
* Helps your employees sign in and access resources in:
  * External resources, such as Microsoft 365, the Azure portal, and thousands of other SaaS applications.
  * Internal resources, such as apps on your corporate network and intranet, along with any cloud apps developed by your own organization.

---

## **Multi-Factor Authentication (MFA)**

* A process where a user is prompted during the sign-in process for an additional form of identification, such as a code on their cellphone or a fingerprint scan.
* Provides an additional layer of security to your Azure AD sign-ins.

---

## **Network Security**

* **Network Security Groups (NSGs):** A basic, stateful, packet filtering firewall that enables you to control traffic to and from Azure resources.
* **Azure Firewall:** A managed, cloud-based network security service that protects your Azure Virtual Network resources. It's a fully stateful firewall as a service with built-in high availability and unrestricted cloud scalability.
* **DDoS Protection:** Protects your Azure resources from Distributed Denial of Service (DDoS) attacks.

---

## **Key Vault**

* A cloud service for securely storing and accessing secrets.
* A secret is anything that you want to tightly control access to, such as API keys, passwords, certificates, or cryptographic keys.

---

## **Module 6 Summary**

* **Shared Responsibility Model:** You and Microsoft are responsible for different aspects of security.
* **Security Center:** Unified security management and threat protection.
* **Azure AD:** Identity and access management.
* **MFA:** Additional layer of security.
* **Network Security:** NSGs, Firewall, DDoS Protection.
* **Key Vault:** Securely store secrets.

---

## **Lab 2: Objectives**

* Implement a Network Security Group (NSG).
* Configure NSG rules to allow and deny traffic.

---

## **Lab 2: Instructions - Implement an NSG**

1. Go to the Azure Portal.
2. Search for "Network security groups".
3. Click "Create".
4. Fill in the required details:
    * Subscription, Resource Group
    * Name, Region
5. Click "Review + create" and then "Create".
6. Associate the NSG with a subnet or a network interface.

---

## **Lab 2: Instructions - Configure NSG rules**

1. Go to your NSG.
2. Click on "Inbound security rules" or "Outbound security rules".
3. Click "Add".
4. Fill in the required details:
    * Source, Source port ranges
    * Destination, Destination port ranges
    * Protocol, Action (Allow or Deny)
    * Priority
5. Click "Add".

---

## **Lab 2: Review and Q&A**

* What did we do in this lab?
* Any questions?

---

## **Lab 2: Completed**

You have successfully implemented an NSG and configured its rules.

---

## **Module 7: Governance and Compliance**

* Azure Policy
* Role-Based Access Control (RBAC)
* Azure Blueprints
* Cost Management and Billing

---

## **Azure Policy**

* A service in Azure that you use to create, assign, and manage policies.
* These policies enforce different rules and effects over your resources, so those resources stay compliant with your corporate standards and service level agreements.

---

## **Role-Based Access Control (RBAC)**

* Helps you manage who has access to Azure resources, what they can do with those resources, and what areas they have access to.
* You can segregate duties within your team and grant only the amount of access to users that they need to perform their jobs.

---

## **Azure Blueprints**

* Enables you to create and manage a library of templates that you can use to deploy and update your applications.
* A blueprint is a package or container for composing focus-specific sets of standards, patterns, and requirements related to the implementation of Azure cloud services, security, and design.

---

## **Cost Management and Billing**

* A suite of tools that help you monitor, control, and optimize your Azure spending.
* Helps you understand your Azure bill, manage your costs and budgets, and optimize your cloud spending.

---

## **Module 7 Summary**

* **Azure Policy:** Enforce rules for your resources.
* **RBAC:** Manage who has access to your resources.
* **Azure Blueprints:** Deploy and update applications in a standardized way.
* **Cost Management and Billing:** Monitor and optimize your Azure spending.

---

## **Final Workshop**

* Create Azure VM (Ubuntu latest)
* [Setup Apache Nginx](https://nginx.org/en/download.html)
* Open port access

---

## **Course Summary**

* **Part 1: Introduction to Cloud Concepts**
  * Cloud Models, Deployment Models, Benefits
* **Part 2: Azure Architecture and Services**
  * Azure Architecture, Core Services (Compute, Networking, Storage, Databases), Azure Solutions
* **Part 3: Azure Management and Governance**
  * Management Tools, Security, Governance, and Compliance

---

## **Exam AZ-900 Preparation**

* This course covered the fundamental concepts of Azure.
* To prepare for the AZ-900 exam, you should:
  * Review the official Microsoft Learn path.
  * Do hands-on labs.
  * Take practice exams.

---

## **Next Steps and Resources**

* **Microsoft Learn:** https://learn.microsoft.com/en-us/training/azure/
* **Azure Documentation:** https://docs.microsoft.com/en-us/azure/
* **Azure YouTube Channel:** https://www.youtube.com/c/msftazure
