# Chapter 13

### 1. Explain the characteristics of Cloud Computing.

- On-demand self-service:

    As a customer for a cloud service provider, you should be able to provision computing capabilities, such as server time and network storage, according to your needs, without requiring assistance from the service provider. 
    
    If you are a cloud service provider like Amazon, you should publish a service catalogue, which contains information about all cloud services available to your customers. The service catalogue should include information about service attributes, prices, and request processes. Customers should be able to view the service catalogue from an online interface and use it to request a service. Consumers can either use one of the “ready-to-use” services or change a few service parameters abd customize them.

- Broad network access:

    Cloud computing services should be available over the network and accessible via several different platforms and devices (for example, mobile phones, tablets, laptops, and workstations).

- Resource Pooling:

    The cloud service provider’s computing resources should be able to be pooled to serve multiple customers using a mode of operation of software where multiple independent instances of one or multiple applications operate in a shared environment model, with different physical and virtual resources dynamically assigned and reassigned according to demand. Customers need not know exactly where resource are located but should be able to specify location at a higher level of abstraction (for example, country, state, or data center). Examples of resources include storage, processing, memory, and network bandwidth.

- Rapid elasticity:

    Services should be elastically provisioned and released to the extent that they are able to scale rapidly outward and inward based on demand. To the customer, the capabilities available for provisioning should be unlimited and possess the ability to be apportioned in any quantity at any time.
    
    Customers should be able to take advantage of rapid elasticity of the cloud when they have a fluctuation in their IT resource requirements. For example, an organization might require double the number of web and application servers for a amount of time to accomplish their tasks. Otherwise, unused resources should automatically be released via load balancers. The cloud enables consumers to grow and shrink the demand for resources dynamically.

- Measured service:

    When customers use cloud services, the cloud service providers should use metrics to determine which resources are being used when and appropriately apportion them for optimal performance (for example, storage, processing,
    bandwidth, and active user accounts). Resource usage should be monitored,
    controlled, and reported, to provide transparency for both the provider
    and consumer of the utilized service.

### 2. Explain the 3 cloud service models.

- IaaS (Infrastructure as a Service):

    The cloud service provider gives the customer the ability to provision processing, storage, networks, and other computing resources onto which they can deploy and run their own software, operating systems, and applications. The customer need not manage or control the underlying cloud infrastructure, but they have full control over their OSs and applications, and limited control of certain networking components (host firewalls).

- PaaS (Platform as a Service):

    The cloud service provider gives the customer the ability to deploy onto the cloud infrastructure customer-created or acquired applications created using programming languages, libraries, services, and tools supported by the provider. The customer doesn't need to manage/control the cloud infrastructure, but they have full control over their deployed applications
    and possibly configuration settings for the application-hosting environment.

- SaaS (Software as a Service):

    The cloud service provider’s applications running on a cloud infrastructure are given to the customer to use. The applications are accessible from several
    client devices through either a thin client interface, such as a web browser (for example, web-based e-mail), or a program interface. The customer does not
    manage or control the underlying cloud infrastructure including network, servers, operating systems, storage, or even individual application capabilities, with the possible exception of limited user-specific application configuration settings.

### 3. What are some of the cloud adoption considerations.

- They are deployment model, compatibility, cost, cloud service provider, and SLAs.

    Deployment model selection in quite important. Public cloud is provisioned for open use by the general public. In a private cloud, the infrastructure is provisioned for exclusive use by a single organization. A community cloud infrastructure is provisioned for exclusive use by a specific community of consumers from organizations that have shared concerns (for example, mission, security requirements, policy, and compliance considerations). A hybrid cloud infrastructure is a composition of two or more distinct cloud infrastructures (private, community, or public) that remain unique entities, but are bound together by standardized or proprietary technology that enables data and application portability (for example, cloud bursting for load balancing between clouds).

    In terms of compatibility, not all applications are good candidates for a
    public cloud. This may be due to the incompatibility between the cloud
    platform software and the consumer applications, or maybe the organization
    plans to move a legacy application to the cloud. Proprietary and mission critical applications are core and essential to the business. They are usually
    designed, developed, and maintained in-house.

    A careful analysis of financial benefits provides a
    clear picture about the cost-savings in adopting the cloud. The analysis
    should compare both the Total Cost of Ownership (TCO) and the Return
    on Investment (ROI) in the cloud and non-cloud environment and identify
    the potential cost benefit.

    When trying find a cloud service provider customers need to find out how long and how well the provider has been delivering the services. They also need
    to determine how easy it is to add or terminate cloud services with the
    service provider. The consumer should know how easy it is to move to
    another provider, when required. They must assess how the provider
    fulfi lls the security, legal, and privacy requirements. They should also
    check whether the provider offers good customer service support.