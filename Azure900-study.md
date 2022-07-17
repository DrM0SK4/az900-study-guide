# Describe cloud concepts

<details>
  <summary>  Describe cloud computing (25—30%)  </summary>

- ### Define cloud computing

  > Cloud computing is the delivery of computing services over the internet.

- ### Describe the shared responsibility model
  > [<img src="https://docs.microsoft.com/en-us/learn/wwl-azure/describe-cloud-compute/media/shared-responsibility-b3829bfe.svg">](http://google.com.au/)
- ### Define cloud models, including public, private, and hybrid
  > | Private                                                           | Public                                                                    | Hybrid                                                                                                                      | Multi-cloud                                                                                                                          |
  > | ----------------------------------------------------------------- | ------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------ |
  > | It’s a cloud built, controlled, and maintained by a single entity | built, controlled, and maintained by a third-party cloud provider         | uses both public and private clouds in an inter-connected environment                                                       | use multiple public cloud providers. Maybe you use different features from different cloud providers                                 |
  > | provides much greater control for the company and greater cost    | anyone that wants to purchase cloud services can access and use resources | users can flexibly choose which services to keep in public cloud and which to deploy to their private cloud infrastructure. | a multi-cloud environment you deal with two (or more) public cloud providers and manage resources and security in both environments. |
  >
  > > Azure Arc: set of technologies that helps manage your cloud environment
- ### Identify appropriate use cases for each cloud model
- ### Describe the consumption-based model

  > | CapEx                                                         | OpEx                                             |
  > | ------------------------------------------------------------- | ------------------------------------------------ |
  > | up-front expenditure to purchase or secure tangible resources | spending money on services or products over time |
  >
  > Cloud computing is opEx: you pay for the IT resources you use which helps you:
  >
  > - Plan and manage your operating costs.
  > - Run your infrastructure more efficiently.
  > - Scale as your business needs change.

- ### Compare cloud pricing models

## Describe the benefits of using cloud services

- ### Describe the benefits of high availability and scalability in the cloud

  > High availability focuses on ensuring maximum availability, regardless of disruptions or events that may occur. These guarantees are part of the service-level agreements (SLAs).

  > Scalability refers to the ability to adjust resources to meet demand
  > | Vertical scaling| Horizontal scaling |
  > | --------------- | ------------------ |
  > | need more processing power (add more CPUs or RAM to a VM) | add additional virtual machines or containers|

- ### Describe the benefits of reliability and predictability in the cloud

  > Reliability is the ability of a system to recover from failures and continue to function.

  > Predictability can be focused on performance predictability or cost predictability.
  > | Performance| Cost |
  > | --------------- | ------------------ |
  > | Autoscaling, load balancing, and high availability are just some of the cloud concepts that support performance predictability | forecasting the cost of the cloud spend|

- ### Describe the benefits of security and governance in the cloud

  > Governance
  >
  > - set templates help ensure that all your deployed resources meet corporate standards and government regulatory requirements.
  > - Cloud-based auditing helps flag any resource that’s out of compliance with your corporate standards and provides mitigation strategies

  > Security
  >
  > - cloud providers are typically well suited to handle things like distributed denial of service (DDoS) attacks
  > - maximum control of security (IAAS): lets you manage the operating systems and installed software
  > - Automatic patches and maintenanance (PAAS):

- ### Describe the benefits of manageability in the cloud
  > In the cloud, you can:
  >
  > - Automatically scale resource deployment based on need.
  > - Deploy resources based on a preconfigured template, removing the need for manual configuration.
  > - Monitor the health of resources and automatically replace failing resources.
  > - Receive automatic alerts based on configured metrics, so you’re aware of performance in real time.
  >   Using diffetent technologies such as:
  > - Through a web portal.
  > - Using a command line interface.
  > - Using APIs.
  > - Using PowerShell.

## Describe cloud service types

- ### Describe infrastructure as a service (IaaS)
  > - most flexible category of cloud services
  > - With IaaS, you’re essentially renting the hardware in a cloud datacenter, , but what you do with that hardware is up to you.
- ### Describe platform as a service (PaaS)
  > - middle ground between renting space in a datacenter (IAAS) and paying for a complete and deployed solution (SAAS)
  > - In a PaaS scenario, you don't have to worry about the licensing or patching for operating systems and databases.
- ### Describe software as a service (SaaS)
  > - The most complete cloud service model from a product perspective. Least flexible, it’s also the easiest to get up and running
  > - you’re essentially renting or using a fully developed application. Email, financial software, messaging applications, and connectivity software are all common examples of a SaaS implementation.
- ### Identify appropriate use cases for each cloud service (IaaS, PaaS, SaaS)
  > Scenarios
  > | IAAS | PAAS | SAAS |
  > | --- | --- | --- |
  > |Lift-and-shift migration: You’re standing up cloud resources similar to your on-prem datacenter, and then simply moving the things running on-prem to running on the IaaS infrastructure. | Development framework: PaaS provides a framework that developers can build upon to develop or customize cloud-based applications | Email and messaging. Business productivity applications |
  > |Testing and development: You have established configurations for development and test environments that you need to rapidly replicate. You can stand up or shut down the different environments rapidly with an IaaS structure, while maintaining complete control. | Analytics or business intelligence: Tools provided as a service with PaaS allow organizations to analyze and mine their data, finding insights and patterns and predicting outcomes to improve forecasting, product design decisions, investment returns, and other business decisions. | Finance and expense tracking |

</details>

<!-- <details> -->
  <summary> Describe Azure architecture and services (35—40%) </summary>

## Describe the core architectural components of Azure

- ### Describe Azure regional, regional pairs, and sovereign regions
- ### Describe availability zones
- ### Describe Azure datacenters
- ### Describe Azure resources and resource groups
- ### Describe subscriptions
- ### Describe management groups
- ### Describe the hierarchy of resource groups, subscriptions, and management groups

## Describe Azure compute and networking services

- ### Compare compute types, including container instances, virtual machines (VMs), and functions
  | Container Instances                                                                                                                       | Virtual Machines                                             | Functions                                                                                                                                                                                                                                                                                                                                                                                     |
  | ----------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
  | Containers are a virtualization environment. <br> You can run multiple containers on a virtual host </br> You don't have to manage the OS | IAAS where you need to set Size, Storage disk and networking | Azure Functions is an event-driven, serverless compute option that doesn’t require maintaining virtual machines or containers. It is ideal when you're only concerned about the code running your service and not about the underlying platform or infrastructure <br> Functions scale automatically based on demand </br> you're only charged for the CPU time used while your function runs |
- ### Describe VM options: including Azure Virtual Machines, Azure Virtual Machine Scale Sets, availability sets, and Azure Virtual Desktop
  > | Azure Virtual Machine scale sets                                                                                                                | Azure Virtual Machine availability sets                                                                                                                                                                            | Azure Virtual Desktop                                                                                                                                                                                                                                                         |
  > | ----------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
  > | let you create and manage a group of identical, load-balanced VMs                                                                               | Availability sets are designed to ensure that VMs stagger updates and have varied power and network connectivity, preventing you from losing all your VMs with a single network or power failure.                  | Is a desktop and application virtualization service that runs on the cloud. It enables you to use a cloud-hosted version of Windows from any location                                                                                                                         |
  > | Scale sets allow you to centrally manage, configure, and update a large number of VMs                                                           | The update domain groups VMs that can be rebooted at the same time. This allows you to apply updates while knowing that only one update domain grouping will be offline at a time                                  | Provides centralized security management for users' desktops with Azure Active Directory. <br> You can enable multifactor authentication to secure user sign-ins. </br> You can also secure access to data by assigning granular role-based access controls (RBACs) to users. |
  > | The number of VM instances can automatically increase or decrease in response to demand, or you can set it to scale based on a defined schedule | The fault domain groups your VMs by common power source and network switch. This helps protect against a physical power or networking failure as the Vms are connected to different power and networking resources | the data and apps are separated from the local hardware. <br> user sessions are isolated in both single and multi-session environments </br>                                                                                                                                  |
- ### Describe resources required for virtual machines
  > - Size (purpose, number of processor cores, and amount of RAM)
  > - Storage disks (hard disk drives, solid state drives, etc.)
  > - Networking (virtual network, public IP address, and port configuration)
- ### Describe application hosting options, including the Web Apps feature of Azure App Service, containers, and virtual machines

  > If you need to host your application on Azure, you might initially turn to a virtual machine (VM) or container. There are other hosting options that you can use with Azure, including Azure App Service. <br>
  > Azure App Service is an HTTP-based service for hosting web applications, REST APIs, and mobile back ends. It offers automatic scaling and high availability
  >
  > - Deployment and management are integrated into the platform.
  > - Endpoints can be secured.
  > - Sites can be scaled quickly to handle high traffic loads.
  > - The built-in load balancing and traffic manager provide high availability.
  >   | Web apps | Api apps | WebJobs | Mobile apps |
  >   | --- | --- | --- | --- |

- ### Describe virtual networking, including the purpose of Azure Virtual Networks, Azure virtual subnets, peering, Azure DNS, Azure VPN Gateway, and Azure ExpressRoute

  > - Azure Virtual Networking and Azure Virtual subnets enable Azure resources, such as VMs, web apps, and databases, to communicate with each other, with users on the internet, and with your on-premises client computers.

  > > Isolation and segmentation:
  > >
  > > > - Azure virtual network allows you to create multiple isolated virtual networks.

  > > Communicate between Azure resources
  > >
  > > > - Virtual networks can connect not only VMs but other Azure resources, such as the App Service Environment for Power Apps, Azure Kubernetes Service, and Azure virtual machine scale sets.
  > > > - Service endpoints can connect to other Azure resource types, such as Azure SQL databases and storage accounts. This approach enables you to link multiple Azure resources to virtual networks to improve security and provide optimal routing between resources

  > > Communicate with on-premises resources
  > >
  > > > Azure virtual networks enable you to link resources together in your on-premises environment and within your Azure subscription. There are three mechanisms for you to achieve this connectivity:
  > >
  > > > - Point-to-site virtual private network connections are from a computer outside your organization back into your corporate network. <br>The client computer initiates an encrypted VPN connection to connect to the Azure virtual network.
  > > > - Site-to-site virtual private networks link your on-premises VPN device or gateway to the Azure VPN gateway in a virtual network. <br> The connection is encrypted and works over the internet.
  > > > - Azure ExpressRoute provides a dedicated private connectivity to Azure that doesn't travel over the internet.

  > > Route network traffic
  > >
  > > > By default, Azure routes traffic between subnets on any connected virtual networks, on-premises networks, and the internet. To ovveride these settings you can:
  > >
  > > > - Route tables allow you to define rules about how traffic should be directed. You can create custom route tables that control how packets are routed between subnets
  > > > - Border Gateway Protocol (BGP) works with Azure VPN gateways, Azure Route Server, or Azure ExpressRoute to propagate on-premises BGP routes to Azure virtual networks.

  > > Filter network traffic
  > >
  > > > Azure virtual networks enable you to filter traffic between subnets by using the following approaches:
  > >
  > > > - Network security groups are Azure resources that can contain multiple inbound and outbound security rules. You can define these rules to allow or block traffic, based on factors such as source and destination IP address, port, and protocol
  > > > - Network virtual appliances are specialized VMs that can be compared to a hardened network appliance. A network virtual appliance carries out a particular network function, such as running a firewall or performing wide area network (WAN) optimization

  > > Connect virtual networks (Peering)
  > >
  > > > You can link virtual networks together by using virtual network peering. These virtual networks can be in separate regions, which allows you to create a global interconnected network through Azure. <br> Peering allows two virtual networks to connect directly to each other. Network traffic between peered networks is private, and travels on the Microsoft backbone network, never entering the public internet. </br>

  > > > User-defined routes (UDR) allow you to control the routing tables between subnets within a virtual network or between virtual networks. This allows for greater control over network traffic flow.

- ### Virtual private networks
  > [link](https://docs.microsoft.com/en-gb/learn/modules/describe-azure-compute-networking-services/10-virtual-private-networks)
- ### Azure ExpressRoute
  > [link](https://docs.microsoft.com/en-gb/learn/modules/describe-azure-compute-networking-services/11-expressroute) <br>
  > Azure ExpressRoute lets you extend your on-premises networks into the Microsoft cloud over a private connection, with the help of a connectivity provider. This connection is called an ExpressRoute Circuit. <br> This allows you to connect offices, datacenters, or other facilities to the Microsoft cloud. Each location would have its own ExpressRoute circuit.
  >
  > - Connectivity can be from an any-to-any (IP VPN) network, a point-to-point Ethernet network, or a virtual cross-connection through a connectivity provider at a colocation facility
  > - ExpressRoute connections don't go over the public Internet. (reliability, faster, consistent latencies, and higher security than typical connections over the Internet)
- ### Azure DNS

  > [link](https://docs.microsoft.com/en-gb/learn/modules/describe-azure-compute-networking-services/12-domain-name-system)
  > Azure DNS is a hosting service for DNS domains that provides name resolution by using Microsoft Azure infrastructure
  >
  > - DNS domains in Azure DNS are hosted on Azure's global network of DNS name servers, providing resiliency and high availability
  > - Azure DNS is based on Azure Resource Manager, which provides features such as:

  > > - Azure role-based access control (Azure RBAC) to control who has access to specific actions for your organization.
  > > - Activity logs to monitor how a user in your organization modified a resource or to find an error when troubleshooting.
  > > - Resource locking to lock a subscription, resource group, or resource. Locking prevents other users in your organization from accidentally deleting or modifying critical resources.
  >
  > - you can manage your domains and records with the Azure portal, Azure PowerShell cmdlets, and the cross-platform Azure CLI. you can also use REST and API

- ### Define public and private endpoints

  > | Public                                                                   | Private                                                                                                             |
  > | ------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------- |
  > | have a public IP address and can be accessed from anywhere in the world. | exist within a virtual network and have a private IP address from within the address space of that virtual network. |

## Describe Azure storage services

- ### Compare Azure storage services
- ### Describe storage tiers
- ### Describe redundancy options
- ### Describe storage account options and storage types
- ### Identify options for moving files, including AzCopy, Azure Storage Explorer, and Azure File Sync
- ### Describe migration options, including Azure Migrate and Azure Data Box
- ### Describe Azure identity, access, and security
- ### Describe directory services in Azure, including Azure Active Directory (Azure AD) and Azure Active Directory Domain Services (Azure AD DS)
- ### Describe authentication methods in Azure, including single sign- ###on (SSO), multifactor authentication, and passwordless
- ### Describe external identities and guest access in Azure
- ### Describe Azure AD Conditional Access
- ### Describe Azure role- ###based access control (RBAC)
- ### Describe the concept of Zero Trust
- ### Describe the purpose of the defense in depth model
- ### Describe the purpose of Microsoft Defender for Cloud

</details>
  
<details>
  <summary> Describe Azure management and governance (30—35%) </summary>

## Describe cost management in Azure

- ### Describe factors that can affect costs in Azure
- ### Compare the Pricing calculator and the Total Cost of Ownership (TCO) calculator
- ### Describe the Azure Cost Management and Billing tool
- ### Describe the purpose of tags

## Describe features and tools in Azure for governance and compliance

- ### Describe the purpose of Azure Blueprints
- ### Describe the purpose of Azure Policy
- ### Describe the purpose of resource locks
- ### Describe the purpose of the Service Trust Portal

## Describe features and tools for managing and deploying Azure resources

- ### Describe the Azure portal
- ### Describe Azure Cloud Shell, including Azure CLI and Azure PowerShell
- ### Describe the purpose of Azure Arc
- ### Describe Azure Resource Manager and Azure Resource Manager templates (ARM templates)

## Describe monitoring tools in Azure

- ### Describe the purpose of Azure Advisor
- ### Describe Azure Service Health
- ### Describe Azure Monitor, including Log Analytics, Azure Monitor alerts, and Application Insights

</details>
