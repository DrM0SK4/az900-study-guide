# AZ 900 study guide

## Describe cloud concepts

<details>
  <summary>  Describe cloud computing (25—30%)  </summary>

- ### Define cloud computing

  > Cloud computing is the delivery of computing services over the internet.

- ### Describe the shared responsibility model

  > ![responsabilty model](https://docs.microsoft.com/en-us/learn/wwl-azure/describe-cloud-compute/media/shared-responsibility-b3829bfe.svg)

- ### Define cloud models, including public, private, and hybrid

  > | Private                                                           | Public                                                                    | Hybrid                                                                                                                      | Multi-cloud                                                                                                                          |
  > | ----------------------------------------------------------------- | ------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------ |
  > | It’s a cloud built, controlled, and maintained by a single entity. It is required to be on a private network | built, controlled, and maintained by a third-party cloud provider         | uses both public and private clouds in an inter-connected environment                                                       | use multiple public cloud providers. Maybe you use different features from different cloud providers                                 |
  > | provides much greater control for the company and greater cost    | anyone that wants to purchase cloud services can access and use resources | users can flexibly choose which services to keep in public cloud and which to deploy to their private cloud infrastructure. | a multi-cloud environment you deal with two (or more) public cloud providers and manage resources and security in both environments. The company can augment on-premises resouces by proviind overflow capaciy.|
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

  > ![iaas paas saas](https://docs.microsoft.com/en-us/learn/azure-fundamentals/fundamental-azure-concepts/media/iaas-paas-saas-575a09e9.png)
  >
  > - most flexible category of cloud services
  > - With IaaS, you’re essentially renting the hardware in a cloud datacenter, , but what you do with that hardware is up to you.
  >
- ### Describe platform as a service (PaaS)
  >
  > - middle ground between renting space in a datacenter (IAAS) and paying for a complete and deployed solution (SAAS)
  > - In a PaaS scenario, you don't have to worry about the licensing or patching for operating systems and databases.
  >
- ### Describe software as a service (SaaS)
  >
  > - The most complete cloud service model from a product perspective. Least flexible, it’s also the easiest to get up and running
  > - you’re essentially renting or using a fully developed application. Email, financial software, messaging applications, and connectivity software are all common examples of a SaaS implementation.
  >
- ### Identify appropriate use cases for each cloud service (IaaS, PaaS, SaaS)

  > Scenarios
  > | IAAS | PAAS | SAAS |
  > | --- | --- | --- |
  > |Lift-and-shift migration: You’re standing up cloud resources similar to your on-prem datacenter, and then simply moving the things running on-prem to running on the IaaS infrastructure. | Development framework: PaaS provides a framework that developers can build upon to develop or customize cloud-based applications | Email and messaging. Business productivity applications |
  > |Testing and development: You have established configurations for development and test environments that you need to rapidly replicate. You can stand up or shut down the different environments rapidly with an IaaS structure, while maintaining complete control. | Analytics or business intelligence: Tools provided as a service with PaaS allow organizations to analyze and mine their data, finding insights and patterns and predicting outcomes to improve forecasting, product design decisions, investment returns, and other business decisions. | Finance and expense tracking |

</details>

<details>
  <summary> Describe Azure architecture and services (35—40%) </summary>

## Describe the core architectural components of Azure

- ### Describe Azure regional, regional pairs, and sovereign regions
  
  > | Regional Pairs | Sovereign Regions |
  > | --- | --- |
  > |  Most Azure regions are paired with another region within the same geography (such as US, Europe, or Asia) at least 300 miles away   |  Sovereign regions are instances of Azure that are isolated from the main instance of Azure. You may need to use a sovereign region for compliance or legal purposes   |
  >
  > -
  >
  > -

- ### Describe availability zones
  >
  > - Availability zones are physically separate datacenters within an Azure region. Each availability zone is made up of one or more datacenters equipped with independent power, cooling, and networking
  > ![availability zone](https://docs.microsoft.com/en-gb/learn/wwl-azure/describe-core-architectural-components-of-azure/media/availability-zones-c22f95a3.png)

- ### Describe Azure datacenters
  >
  > - the datacenters are the same as large corporate datacenters. They’re facilities with resources arranged in racks, with dedicated power, cooling, and networking infrastructure

- ### Describe Azure resources and resource groups

  > ![azure resources and resource groups](https://docs.microsoft.com/en-gb/learn/wwl-azure/describe-core-architectural-components-of-azure/media/account-scope-levels-9ceb3abd.png)
  >
  > - A resource is the basic building block of Azure. Anything you create, provision, deploy, etc. is a resource
  > - Resource groups are simply groupings of resources. When you create a resource, you’re required to place it into a resource group. While a resource group can contain many resources, a single resource can only be in one resource group at a time.
  > - When you apply an action to a resource group, that action will apply to all the resources within the resource group
  > - If you delete a resource group, all the resources will be deleted
  > - If you grant or deny access to a resource group, you’ve granted or denied access to all the resources within the resource group

- ### Describe subscriptions

  > - subscriptions are a unit of management, billing, and scale. Similar to how resource groups are a way to logically organize resources, subscriptions allow you to logically organize your resource groups and facilitate billing.
  > - An account can have multiple subscriptions, but it’s only required to have one
  > - A subscription provides you with authenticated and authorized access to Azure products and services.
  > - You can use Azure subscriptions to define boundaries around Azure products, services, and resources
  >
  >  | Billing boundary | Access control boundary |
  >  | --- | --- |
  >  | determines how an Azure account is billed for using Azure     |  Azure applies access-management policies at the subscription level, and you can create separate subscriptions to reflect different organizational structures   |
  >  |  You can create multiple subscriptions for different types of billing requirements | This billing model allows you to manage and control access to the resources that users provision with specific subscriptions|
  >
  > - You can create additional subscription to sepearate:
  > >
  > > - Environments: to setup separate enviroments for prod and dev
  > > - Organizational structures: to manage contorl access to resoruces for users in different subscriptions
  > > - Billing: separate billing for prod and dev
  > >
- ### Describe management groups
  >
  > - Azure management groups provide a level of scope above subscriptions.  You organize subscriptions into containers called management groups and apply governance conditions to the management groups.
  > - All subscriptions within a management group automatically inherit the conditions applied to the management group
  >

- ### Describe the hierarchy of resource groups, subscriptions, and management groups
  >
  > - ![mgmt groups, subscriptions and resource group hierarchy](https://docs.microsoft.com/en-gb/learn/wwl-azure/describe-core-architectural-components-of-azure/media/management-groups-subscriptions-dfd5a108.png)
  >
## Describe Azure compute and networking services

- ### Compare compute types, including container instances, virtual machines (VMs), and functions

  | Container Instances                                                                                                                       | Virtual Machines                                             | Functions                                                                                                                                                                                                                                                                                                                                                                                     |
  | ----------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
  | Containers are a virtualization environment.\
   You can run multiple containers on a virtual host\
   You don't have to manage the OS | IAAS where you need to set Size, Storage disk and networking | Azure Functions is an event-driven, serverless compute option that doesn’t require maintaining virtual machines or containers. It is ideal when you're only concerned about the code running your service and not about the underlying platform or infrastructure\
    Functions scale automatically based on demand\
   you're only charged for the CPU time used while your function runs |

- ### Describe VM options: including Azure Virtual Machines, Azure Virtual Machine Scale Sets, availability sets, and Azure Virtual Desktop

  > | Azure Virtual Machine scale sets                                                                                                                | Azure Virtual Machine availability sets                                                                                                                                                                            | Azure Virtual Desktop                                                                                                                                                                                                                                                         |
  > | ----------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
  > | let you create and manage a group of identical, load-balanced VMs                                                                               | Availability sets are designed to ensure that VMs stagger updates and have varied power and network connectivity, preventing you from losing all your VMs with a single network or power failure.                  | Is a desktop and application virtualization service that runs on the cloud. It enables you to use a cloud-hosted version of Windows from any location                                                                                                                         |
  > | Scale sets allow you to centrally manage, configure, and update a large number of VMs                                                           | The update domain groups VMs that can be rebooted at the same time. This allows you to apply updates while knowing that only one update domain grouping will be offline at a time                                  | Provides centralized security management for users' desktops with Azure Active Directory.\
   You can enable multifactor authentication to secure user sign-ins. An azure multi-factor authentication server is ONLY REQUIRED for authentication when support users locate on on-premises Active Directory \
   You can also secure access to data by assigning granular role-based access controls (RBACs) to users. |
  > | The number of VM instances can automatically increase or decrease in response to demand, or you can set it to scale based on a defined schedule | The fault domain groups your VMs by common power source and network switch. This helps protect against a physical power or networking failure as the Vms are connected to different power and networking resources | the data and apps are separated from the local hardware.\
   user sessions are isolated in both single and multi-session environments\
                                                                                                                                    |

- ### Describe resources required for virtual machines
  >
  > - Size (purpose, number of processor cores, and amount of RAM)
  > - Storage disks (hard disk drives, solid state drives, etc.)
  > - Networking (virtual network, public IP address, and port configuration)
  >
- ### Describe application hosting options, including the Web Apps feature of Azure App Service, containers, and virtual machines

  > If you need to host your application on Azure, you might initially turn to a virtual machine (VM) or container. There are other hosting options that you can use with Azure, including Azure App Service.\
  >
  > Azure App Service is an HTTP-based service for hosting web applications, REST APIs, and mobile back ends. It offers automatic scaling and high availability
  >
  > - Deployment and management are integrated into the platform.
  > - Endpoints can be secured.
  > - Sites can be scaled quickly to handle high traffic loads.
  > - The built-in load balancing and traffic manager provide high availability.
  >   | Web apps | Api apps | WebJobs | Mobile apps |
  >
  >   | --- | --- | --- | --- |

- ### Describe virtual networking, including the purpose of Azure Virtual Networks, Azure virtual subnets, peering, Azure DNS, Azure VPN Gateway, and Azure ExpressRoute

  > - Azure Virtual Networking and Azure Virtual subnets enable Azure resources, such as VMs, web apps, and databases, to communicate with each other, with users on the internet, and with your on-premises client computers.
  >
  > > Isolation and segmentation:
  > >
  > > > - Azure virtual network allows you to create multiple isolated virtual networks.
  > > Communicate between Azure resources
  > > > - Virtual networks can connect not only VMs but other Azure resources, such as the App Service Environment for Power Apps, Azure Kubernetes Service, and Azure virtual machine scale sets.
  > > > - Service endpoints can connect to other Azure resource types, such as Azure SQL databases and storage accounts. This approach enables you to link multiple Azure resources to virtual networks to improve security and provide optimal routing between resources
  > > Communicate with on-premises resources
  > > > Azure virtual networks enable you to link resources together in your on-premises environment and within your Azure subscription. There are three mechanisms for you to achieve this connectivity:
  > > > - Point-to-site virtual private network connections are from a computer outside your organization back into your corporate network.\
  The client computer initiates an encrypted VPN connection to connect to the Azure virtual network.
  > > > - Site-to-site virtual private networks link your on-premises VPN device or gateway to the Azure VPN gateway in a virtual network.\
   The connection is encrypted and works over the internet.
  > > > - Azure ExpressRoute provides a dedicated private connectivity to Azure that doesn't travel over the internet.
  >>> ![express route](https://docs.microsoft.com/en-us/learn/azure-fundamentals/azure-networking-fundamentals/media/azure-connectivity-models-4deabab1.png)
  > > Route network traffic
  > > > By default, Azure routes traffic between subnets on any connected virtual networks, on-premises networks, and the internet. To ovveride these settings you can:
  > > >
  > > > - Route tables allow you to define rules about how traffic should be directed. You can create custom route tables that control how packets are routed between subnets
  > > > - Border Gateway Protocol (BGP) works with Azure VPN gateways, Azure Route Server, or Azure ExpressRoute to propagate on-premises BGP routes to Azure virtual networks.
  > > Filter network traffic
  > > > Azure virtual networks enable you to filter traffic between subnets by using the following approaches:
  > > >
  > > > - Network security groups are Azure resources that can contain multiple inbound and outbound security rules. You can define these rules to allow or block traffic, based on factors such as source and destination IP address, port, and protocol
  > > > - Network virtual appliances are specialized VMs that can be compared to a hardened network appliance. A network virtual appliance carries out a particular network function, such as running a firewall or performing wide area network (WAN) optimization
  > > Connect virtual networks (Peering)
  > > > You can link virtual networks together by using virtual network peering. These virtual networks can be in separate regions, which allows you to create a global interconnected network through Azure.\
   Peering allows two virtual networks to connect directly to each other. Network traffic between peered networks is private, and travels on the Microsoft backbone network, never entering the public internet.\
  > > > User-defined routes (UDR) allow you to control the routing tables between subnets within a virtual network or between virtual networks. This allows for greater control over network traffic flow.

- ### Virtual private networks

  > [link](https://docs.microsoft.com/en-gb/learn/modules/describe-azure-compute-networking-services/10-virtual-private-networks)
  >
  > - uses an encrypted tunnel within another network. VPNs are typically deployed to connect two or more trusted private networks to one another over an untrusted network (typically the public internet)\
   Traffic is encrypted while traveling over the untrusted network to prevent eavesdropping or other attacks. VPNs can enable networks to safely and securely share sensitive information

- ### VPN gateways

  > A VPN gateway is a type of virtual network gateway. Azure VPN Gateway instances are deployed in a dedicated subnet of the virtual network and enable the following connectivity
  >
  > - Connect on-premises datacenters to virtual networks through a site-to-site connection.
  > - Connect individual devices to virtual networks through a point-to-site connection.
  > - Connect virtual networks to other virtual networks through a network-to-network connection
  > When you deploy a VPN gateway, you specify the VPN type: either policy-based or route-based
  > | Policy-based VPN |  Route-based gateways |
  > | --- | --- |
  > |  specify statically the IP address of packets that should be encrypted through each tunnel |  IP routing (either static routes or dynamic routing protocols) decides which one of these tunnel interfaces to use when sending each packet. are the preferred connection method for on-premises devices |
  > | | Connections between virtual networks\
   Point-to-site connections\
   Multisite connections\
   Coexistence with an Azure ExpressRoute gateway  |
  > By default, VPN gateways are deployed as two instances in an active/standby
  
- ### Azure ExpressRoute

  > [link](https://docs.microsoft.com/en-gb/learn/modules/describe-azure-compute-networking-services/11-expressroute)\
  >
  > Azure ExpressRoute lets you extend your on-premises networks into the Microsoft cloud over a private connection, with the help of a connectivity provider. This connection is called an ExpressRoute Circuit.\
  > IT IS NOT USED TO SECURE TRAFFIC BETWEEN PRIVATE NETWORKS
   This allows you to connect offices, datacenters, or other facilities to the Microsoft cloud. Each location would have its own ExpressRoute circuit.
  >
  > - Connectivity can be from an any-to-any (IP VPN) network, a point-to-point Ethernet network, or a virtual cross-connection through a connectivity provider at a colocation facility
  > - ExpressRoute connections don't go over the public Internet. (reliability, faster, consistent latencies, and higher security than typical connections over the Internet)
  >
- ### Azure DNS

  > [link](https://docs.microsoft.com/en-gb/learn/modules/describe-azure-compute-networking-services/12-domain-name-system)
  > Azure DNS is a hosting service for DNS domains that provides name resolution by using Microsoft Azure infrastructure
  >
  > - DNS domains in Azure DNS are hosted on Azure's global network of DNS name servers, providing resiliency and high availability
  > - Azure DNS is based on Azure Resource Manager, which provides features such as:
  >
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
  >
  >
  > - Redundancy ensures that your storage account meets its availability and durability targets even in the face of failures.
  > - Redundancy in the primary region:
  > Data in an Azure Storage account is always replicated three times in the primary region
  >
  >> - Locally redundant storage: LRS is the lowest-cost redundancy option and offers the least durability compared to other options.\
  LRS provides at least 11 nines of durability (99.999999999%) of objects over a given year.
  >> - Zone-redundant storage: ZRS replicates your Azure Storage data synchronously across three Azure availability zones in the primary region.\
  ZRS offers durability for Azure Storage data objects of at least 12 nines (99.9999999999%) over a given year
  >>
  > - Redundancy in a secondary region:
  > For applications requiring high durability, you can choose to additionally copy the data in your storage account to a secondary region that is hundreds of miles away from the primary region
  >
  >> - Geo-redundant storage:  GRS copies your data synchronously three times within a single physical location in the primary region using LRS. It then copies your data asynchronously to a single physical location in the secondary region (the region pair) using LRS\
  GRS offers durability for Azure Storage data objects of at least 16 nines (99.99999999999999%) over a given year
  >> - Geo-zone-redundant storage:  Data in a GZRS storage account is copied across three Azure availability zones in the primary region (similar to ZRS) and is also replicated to a secondary geographic region, using LRS, for protection from regional disaster
  >>
- ### Describe storage account options and storage types

  > |Azure Blobs| Azure Files | Azure Queues | Azure Disks |
  > | --- | ---| ---| ---|
  > | A massively scalable object store for text and binary data. Also includes support for big data analytics through Data Lake Storage Gen2 | Managed file shares for cloud or on-premises deployments | A messaging store for reliable messaging between application components | Block-level storage volumes for Azure VMs.  Azure Files ensures the data is encrypted at rest, and the SMB protocol ensures the data is encrypted in transit. |
  > | URLs, the Azure Storage REST API, Azure PowerShell, Azure CLI, or an Azure Storage client library |  PowerShell cmdlets and Azure CLI can be used to create, mount, and manage Azure file shares as well as Azure portal and Azure Storage Explore.  | |  |
  > | | | |
  >>
  > - Blob storage tiers:
  >>
  >> - Hot access tier: Optimized for storing data that is accessed frequently (for example, images for your website).
  >>
  >> - Cool access tier: Optimized for data that is infrequently accessed and stored for at least 30 days (for example, invoices for your customers).
  >>
  >> - Archive access tier: Appropriate for data that is rarely accessed and stored for at least 180 days, with flexible latency requirements (for example, long-term backups).
  >>
  >> - Only the hot and cool access tiers can be set at the account level. The archive access tier isn't available at the account level.
  >>
- ### Identify options for moving files, including AzCopy, Azure Storage Explorer, and Azure File Sync

  > | AZCopy | Azure Storage Explorer | Azure File Sync |
  > | --- | --- | --- |
  > | command-line utility that you can use to copy blobs or files to or from your storage account    | standalone app that provides a graphical interface to manage files and blobs in your Azure Storage Account. It works on Windows, macOS, and Linux.     |  tool that lets you centralize your file shares in Azure Files and keep the flexibility, performance, and compatibility of a Windows file server.  it will automatically stay bi-directionally synced with your files in Azure   |

- ### Describe migration options, including Azure Migrate and Azure Data Box
  >
  > - Azure Migrate: migrate from an on-premises environment to the cloud
  > - Azure Data Box: physical migration service that helps transfer large amounts of data(data sizes larger than 40 TB).
  >

## Describe Azure identity, access, and security

- ### Describe directory services in Azure, including Azure Active Directory (Azure AD) and Azure Active Directory Domain Services (Azure AD DS)
  >
  > - Azure Active Directory (Azure AD) is a directory service that enables you to sign in and access both Microsoft cloud applications and cloud applications that you develop. It is Microsoft's cloud-based identity and access management service.  Azure AD can detect sign-in attempts from unexpected locations or unknown devices
  > - Choose premium if you want to piublish on-premises web apps using AD and if you want your on-premise user to be able to reset their own password. SSO is available with free
  > - Services offered by Azure AD:
  >  
  > | Authentication | Single sign-on | Application Management | Device Management |
  > | --- | --- | --- | --- |
  > | verifying identity to access applications and resources | enables you to remember only one username and one password to access multiple applications | You can manage your cloud and on-premises apps | supports the registration of devices. Registration enables devices to be managed through tools like Microsoft Intune
  >
  > - One method of connecting Azure AD with your on-premises AD is using Azure AD Connect
  > - Azure AD Connect synchronizes changes between both identity systems, so you can use features like SSO, multifactor authentication, and self-service password reset under both systems.
  >
  > - Azure Active Directory Domain Services: is a service that provides managed domain services such as domain join, group policy, lightweight directory access protocol (LDAP), and Kerberos/NTLM authentication
  > - An Azure AD DS managed domain lets you run legacy applications in the cloud that can't use modern authentication method
  > - Azure AD DS integrates with your existing Azure AD tenant. This integration lets users sign into services and applications connected to the managed domain using their existing credentials

- ### Describe authentication methods in Azure, including single sign-on (SSO), multifactor authentication, and passwordless
  >
  > - Authentication is the process of establishing the identity of a person, service, or device. It requires the person, service, or device to provide some type of credential to prove who they are.
  > - Single sign-on (SSO) enables a user to sign in one time and use that credential to access multiple resources and applications from different providers. For SSO to work, the different applications and providers must trust the initial authenticator
  > - Multifactor authentication is the process of prompting a user for an extra form (or factor) of identification during the sign-in process.
  > - Azure AD Multi-Factor Authentication is a Microsoft service that provides multifactor authentication capabilities. It provides an additional form of authentication during sign-in, such as a phone call or mobile app notification
  > - Passwordless authentication methods are more convenient because the password is removed and replaced with something you have, plus something you are, or something you know
  >
  >
- ### Describe external identities and guest access in Azure
  >
  > - An external identity is a person, device, service, etc. that is outside your organization. Azure AD External Identities refers to all the ways you can securely interact with users outside of your organization
  >
- ### Describe Azure AD Conditional Access
  >
  > - Conditional Access is a tool that Azure Active Directory uses to allow (or deny) access to resources based on identity signals\
  A user might not be challenged for second authentication factor if they're at a known location. However, they might be challenged for a second authentication factor if their sign-in signals are unusual or they're at an unexpected location
  >
- ### Describe Azure role-based access control (RBAC)
  >
  > - Azure RBAC provides built-in roles that describe common access rules for cloud resources.
  > - Role-based access control is applied to a scope, which is a resource or set of resources that this access applies to.\
  ![rbac](https://docs.microsoft.com/en-gb/learn/wwl-azure/describe-azure-identity-access-security/media/role-based-access-scope-4b12a8f3.png)
  > - Azure RBAC is hierarchical, in that when you grant access at a parent scope, those permissions are inherited by all child scopes
  > - Azure RBAC is enforced on any action that's initiated against an Azure resource that passes through Azure Resource Manage
  >
- ### Describe the concept of Zero Trust
  >
  > - Zero Trust is a security model that assumes the worst case scenario and protects resources with that expectation
  > - Trust security model, which is based on these guiding principles:
  >
  >|Verify explicitly | Use least privilege access| Assume breach|
  > |---|---|---|
  > |Always authenticate and authorize based on all available data points.| Limit user access with Just-In-Time and Just-Enough-Access (JIT/JEA), risk-based adaptive policies, and data protection.|  Minimize blast radius and segment access. Verify end-to-end encryption. Use analytics to get visibility, drive threat detection, and improve defenses.|

- ### Describe the purpose of the defense in depth model
  >
  > - The objective of defense-in-depth is to protect information and prevent it from being stolen by those who aren't authorized to access it.\
  A defense-in-depth strategy uses a series of mechanisms to slow the advance of an attack that aims at acquiring unauthorized access to data.
  >
  > ![in-depth defense](https://docs.microsoft.com/en-gb/learn/wwl-azure/describe-azure-identity-access-security/media/defense-depth-486afc12.png)
  >
  > - Each layer provides protection so that if one layer is breached, a subsequent layer is already in place to prevent further exposure. This approach removes reliance on any single layer of protection.
  >
  > | The physical security layer | The identity and access layer| The perimeter layer | The network layer | The compute layer| The application layer | The data layer|  
  > |---| --- | ---| --- | ---| --- |---|
  > |the first line of defense to protect computing hardware in the datacenter |controls access to infrastructure and change control | uses distributed denial of service (DDoS) protection to filter large-scale attacks before they can cause a denial of service for users | limits communication between resources through segmentation and access controls. | secures access to virtual machines.| helps ensure that applications are secure and free of security vulnerabilities. | controls access to business and customer data that you need to protect |

- ### Describe the purpose of Microsoft Defender for Cloud
>
> - Defender for Cloud is a monitoring tool for security posture management and threat protection. It monitors your cloud, on-premises, hybrid, and multi-cloud environments to provide guidance and notifications aimed strengthening your security posture
> - in the regulatory compliance dashboard you can see the number of passing and failing assesments and overall complaince score
> - ![defender for cloud](https://docs.microsoft.com/en-us/azure/defender-for-cloud/media/secure-score-security-controls/single-secure-score-via-mobile.png)
> - When necessary, Defender for Cloud can automatically deploy a Log Analytics agent to gather security-related data.\
For Azure machines, deployment is handled directly.\
For hybrid and multi-cloud environments, Microsoft Defender plans are extended to non Azure machines with the help of Azure Arc
> - Recommendations help you reduce the attack surface across each of your resources.
> - The list of recommendations is enabled and supported by the Azure Security Benchmark.\
This Microsoft-authored, Azure-specific, benchmark provides a set of guidelines for security and compliance best practices based on common compliance frameworks.
> - Defender for Cloud groups the recommendations into security controls and adds a secure score value to each control
> - Defender for Cloud fills three vital needs as you manage the security of your resources and workloads in the cloud and on-premises:
>>
>> - Continuously assess: Know your security posture.\
Identify and track vulnerabilities.
>> - Secure: Harden resources and services with Azure Security Benchmark.
>> - Defend: Detect and resolve threats to resources, workloads, and services.

</details>
  
<details>
  <summary> Explore Azure database and analytics services </summary>

## Descibe azure databases and analytics services

- ### Explore Azure SQL Database
  >
  > - Azure SQL Database is a platform as a service (PaaS) database engine. It handles most of the database-management functions — such as upgrading, patching, backups, and monitoring — without user involvemen
  > - You can migrate your existing SQL Server databases with minimal downtime by using the Azure Database Migration Service
  >
<details>
  <summary> Describe Azure management and governance (30—35%) </summary>

## Describe cost management in Azure

- ### Describe factors that can affect costs in Azure
  >
  > - That OpEx cost can be impacted by many factors. Some of the impacting factors are:
  >
  > |Resource type | Consumption | Maintenance | Geography | Subscription type | Azure Marketplace |
  > | --- | --- |--- |--- |--- |--- |
  > || If you use more compute this cycle, you pay more. If you use less in the current cycle, you pay less||Creating the same storage account in different regions may show different costs |Some Azure subscription types also include usage allowances, which affect costs.||
  > ||Azure also offers the ability to commit to using a set amount of cloud resources in advance and receiving discounts on those “reserved” resources||| Azure free trial subscription provides access to a number of Azure products that are free for 12 months. It also includes credit to spend within your first 30 days of sign-up. You'll get access to more than 25 products that are always free (based on resource and region availability).||

- ### Compare the Pricing calculator and the Total Cost of Ownership (TCO) calculator
  >
  > - The pricing calculator is designed to give you an estimated cost for provisioning resources in Azure.\
  The pricing calculator’s focus is on the cost of provisioned resources in Azure.
  > - The TCO calculator is designed to help you compare the costs for running an on-premises infrastructure compared to an Azure Cloud infrastructure
  > - The TCO calculator involves three step
  > ![Tco calculator steps](https://docs.microsoft.com/en-gb/learn/wwl-azure/describe-cost-management-azure/media/total-cost-ownership-calculator-steps-76e927a5.png)
  >
- ### Describe the Azure Cost Management and Billing tool
  >
  > - Cost Management is a SAAS that provides the ability to quickly check Azure resource costs, create alerts based on resource spend, and create budgets that can be used to automate management of resources.
  > Cost analysis is a subset of Cost Management that provides a quick visual for your Azure costs.\
  It allows you to  analyze your organizational costs. You can view aggregated costs by organization to understand where costs are accrued and to identify spending trends
  > Cost alerts provide a single location to quickly check on all of the different alert types that may show up in the Cost Management service. Three types of alerts:
  >
  > | Budget | Credit |  Department spending quota|
  > | --- | --- | --- |
  > | notify you when spending, based on usage or cost, reaches or exceeds the amount defined in the alert condition of the budget. | Credit alerts notify you when your Azure credit monetary commitments are consumed| Department spending quota alerts notify you when department spending reaches a fixed threshold of the quota|
  > |Budget alerts are generated automatically whenever the budget alert conditions are met|Credit alerts are generated automatically at 90% and at 100% of your Azure credit balance|Whenever a threshold is met, it generates an email to department owners, and appears in cost alerts|
  >
  > - A budget is where you set a spending limit for Azure. You can set budgets based on a subscription, resource group, service type, or other criteria. When you set a budget, you will also set a budget alert. When the budget hits the budget alert level, it will trigger a budget alert that shows up in the cost alerts area.
  > - Azure Reservations are a benefit offered by Microsoft that can save you up to 72% as compared to pay-as-you-go prices.
  >
- ### Describe the purpose of tags
  >
  > - Tags provide extra information, or metadata, about your resources. It is a way to organize resources.
  > - You can add, modify, or delete resource tags through Windows PowerShell, the Azure CLI, Azure Resource Manager templates, the REST API, or the Azure portal.
  > - You can use Azure Policy to enforce tagging rules and conventions.

## Describe features and tools in Azure for governance and compliance

- ### Describe the purpose of Azure Blueprints
  >
  > - Azure Blueprints lets you standardize cloud subscription or environment deployments. Instead of having to configure features like Azure Policy for each new subscription, with Azure Blueprints you can define repeatable settings and policies that are applied as new subscriptions are created
  > - Azure Blueprints are version-able
  > - Blueprints are JSON files

- ### Describe the purpose of Azure Policy
  >
  > - Azure Policy is a service in Azure that enables you to create, assign, and manage policies that control or audit your resources
  > - Azure Policy enables you to define both individual policies and groups of related policies, known as initiatives
  > - Azure Policies are inherited, so if you set a policy at a high level, it will automatically be applied to all of the groupings that fall within the parent
  > - An Azure Policy initiative is a way of grouping related policies together. The initiative definition contains all of the policy definitions to help track your compliance state for a larger goal

- ### Describe the purpose of resource locks
  >
  > - A resource lock prevents resources from being accidentally deleted or changed.
  > - two types of resource locks:
  >>
  >> - Delete means authorized users can still read and modify a resource, but they can't delete the resource.
  >> - ReadOnly means authorized users can read a resource, but they can't delete or update the resource. Applying this lock is similar to restricting all authorized users to the permissions granted by the Reader role
  > You can manage resource locks from the Azure portal, PowerShell, the Azure CLI, or from an Azure Resource Manager templat

- ### Describe the purpose of the Service Trust Portal
  >
  > - The Microsoft Service Trust Portal is a portal that provides access to various content, tools, and other resources about Microsoft security, privacy, and compliance practices.

## Describe features and tools for managing and deploying Azure resources

- ### Describe the Azure portal
  >
  > - The Azure portal is a web-based, unified console that provides an alternative to command-line tools. With the Azure portal, you can manage your Azure subscription by using a graphical user interface

- ### Describe Azure Cloud Shell, including Azure CLI and Azure PowerShell
  >
  > - Azure Cloud Shell is a browser-based shell tool that allows you to create, configure, and manage Azure resources using a shell. Azure Cloud Shell support both Azure PowerShell and the Azure Command Line Interface (CLI), which is a Bash shell
  > - Azure PowerShell is a shell with which developers, DevOps, and IT professionals can run commands called command-lets (cmdlets). These commands call the Azure REST API to perform management tasks in Azure
  > - The Azure CLI is functionally equivalent to Azure PowerShell, with the primary difference being the syntax of commands. While Azure PowerShell uses PowerShell commands, the Azure CLI uses Bash commands.

- ### Describe the purpose of Azure Arc
  >
  > - Azure Arc simplifies governance and management by delivering a consistent multi-cloud and on-premises management platform
  > - Azure Arc provides a centralized, unified way to:
  >
  >> - Manage your entire environment together by projecting your existing non-Azure resources into ARM.
  >> - Manage multi-cloud and hybrid virtual machines, Kubernetes clusters, and databases as if they are running in Azure.
  >> - Use familiar Azure services and management capabilities, regardless of where they live.
  >> - Continue using traditional ITOps while introducing DevOps practices to support new cloud and native patterns in your environment.
  >> - Configure custom locations as an abstraction layer on top of Azure Arc-enabled Kubernetes clusters and cluster extensions.

- ### Describe Azure Resource Manager and Azure Resource Manager templates (ARM templates)
  >
  > - Azure Resource Manager (ARM) is the deployment and management service for Azure. It provides a management layer that enables you to create, update, and delete resources in your Azure account
  > - A Resource Manager template is a JSON file that defines what you want to deploy to Azure
  > - ARM templates are another example of infrastructure as code at work.
  > - ou can describe the resources you want to use in a declarative JSON format. With an ARM template, the deployment code is verified before any code is run
  >
  >
## Describe monitoring tools in Azure

- ### Describe the purpose of Azure Advisor
  >
  > - Azure Advisor evaluates your Azure resources and makes recommendations to help improve reliability, security, and performance
  > - Azure Advisor integrates with Microsoft Defender for Cloud to help prevent, detetct and respond to threats to Azure resources.
  > - The recommendations are available via the Azure portal and the API, and you can set up notifications to alert you to new recommendations.
  > - When you're in the Azure portal, the Advisor dashboard displays personalized recommendations for all your subscriptions
  >
  > | Reliability| Security |  Performance  |Operational Excellence  |Cost |
  > | --- |--- |--- |--- |--- |

- ### Describe Azure Service Health
  >
  > - Azure Service Health helps you keep track of Azure resource, both your specifically deployed resources and the overall status of Azure.  Azure service health does this by combining three different Azure services
  >
  > | Azure Status | Service Health|Resource Health |
  > | --- | --- | --- |
  > |is a broad picture of the status of Azure globally. Azure status informs you of service outages in Azure on the Azure Status page | provides a narrower view of Azure services and regions. It focuses on the Azure services and regions you're using. You can even set up Service Health alerts to notify you when service issues, planned maintenance, or other changes may affect the Azure services and regions you use | is a tailored view of your actual Azure resources. It provides information about the health of your individual cloud resources, such as a specific virtual machine instance. Using Azure Monitor, you can also configure alerts to notify you of availability changes to your cloud resources. |

- ### Describe Azure Monitor, including Log Analytics, Azure Monitor alerts, and Application Insights
  >
  > - Azure Monitor is a platform for collecting data on your resources, analyzing that data, visualizing the information, and even acting on the result
  > - Azure Log Analytics is the tool in the Azure portal where you’ll write and run log queries on the data gathered by Azure Monitor
  > - Azure Monitor Alerts are an automated way to stay informed when Azure Monitor detects a threshold being crossed. You set the alert conditions, the notification actions, and then Azure Monitor Alerts notifies when an alert is triggered
  > - Azure Monitor Alerts use action groups to configure who to notify and what action to take. An action group is simply a collection of notification and action preferences that you associate with one or multiple alerts.
  >>
  >> - Application Insights, an Azure Monitor feature, monitors your web applications. Application Insights is capable of monitoring applications that are running in Azure, on-premises, or in a different cloud environment.
  >>

</details>
