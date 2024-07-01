Question: What is the official name of the hardware offering?

Answer: IBM Storage Fusion HCI System is the name of the hardware. Three additional software parts get installed to complete a solution:
- Red Hat® OpenShift® Container Platform
- IBM Storage Fusion HCI System Management Software 
- IBM Storage Fusion HCI System Storage Software

Question: Does IBM Storage Fusion HCI System support both Red Hat OpenShift and VMware?

Answer: Red Hat OpenShift Virtualization supports both native VMWare images and converted OpenShift VM images. IBM Storage Fusion HCI System is a perfect platform to run both Virtual Machines and Containers. Acquire guidance on what virtual workloads work best on OpenShift with IBM Storage Fusion HCI System.
For more information about Red HatOpenShift Virtualization, see OpenShift documentation.

Question: Can IBM Storage Fusion HCI System with OpenShift Virtualization be used to migrate clients off VMware?

Answer: Not directly. OpenShift Virtualization is not a general-purpose replacement for VMware. It is commonly used by teams that want to target specific VMs and enable them to be managed as native Kubernetes objects. OpenShift Virtualization supports Windows and Linux guest operating systems.

Question: Differences between the IBM Storage Fusion HCI System and IBM Storage Fusion versions? 

Answer: IBM Storage Fusion can be deployed two different ways:
- IBM Storage Fusion is an operator that is installed on Red Hat OpenShift Container Platform.
- IBM Storage Fusion HCI System is an entire rack of devices (servers, switches, and so on) which will have Red Hat OpenShift Container Platform and IBM Storage Fusion software installed on it.
User experience varies because of those different deployment models:
- IBM Storage Fusion HCI System has hardware-centric experience and features (monitoring, troubleshooting, adding drives/nodes), whereas forIBM Storage Fusion, those actions take place in Red Hat OpenShift Container Platform.
- The storage management experience between IBM Storage Fusion HCI System and IBM Storage Fusion will vary. IBM Storage Fusion HCI System lets you define multiple storage classes but you can only have one file system.

Question: What is the difference between IBM Storage Fusion HCI System and Cloud Pak System? Is IBM Storage Fusion HCI System a replacement for Cloud Pak System?

Answer: IBM Storage Fusion HCI System provides a cost-effective computing platform, comprised of storage rich servers and network hardware, for OpenShift container-based workloads. It is easy to deploy, simple to maintain, and easy to scale-out capacity as workload demand grows. IBM Storage Fusion HCI System is purpose-built for modern container-based workloads and makes it easy for Infrastructure and Operations (I&O) teams to achieve cloud operating models in their private datacenters. As IBM Storage Fusion HCI System is purpose-built for modern container-based workloads, it eliminates unnecessary baggage and operational complexity of systems that were designed for last-generation VM based workloads. The Cloud Pak System is designed to run VM based applications on VMware.

Question: Where can I learn more about IBM Storage Fusion HCI System and IBM Storage Fusion?

Answer: You can see IBM Documentation at https://www.ibm.com/docs/en/storage-fusion/2.6.

Question: What is supported to run IBM Storage Fusion HCI System in a customer supplied rack?

Answer: There is a recommended option of purchasing IBM Storage Fusion HCI System without a rack.

Question: What is the reasoning behind having 6 PDUs for all config? Why do you have to configure 6 PDUs in econfig?

Answer: IBM Storage Fusion HCI System no longer ships 6 PDUs instead only the number of PDUs that are needed are shipped. The number of PDUs that need to be energized depends on the specific rack configuration.
For more information, see Hardware overview of a single rack.

Question: IBM Storage Fusion HCI System has which OS (Red Hat core OS or RHEL)?

Answer: IBM Storage Fusion HCI System uses CoreOS as the base platform to deploy Red Hat OpenShift Clusters.

Question: IBM Storage Fusion HCI System comes with preinstalled Red Hat OpenShift or do we have to deploy it? 

Answer: It has a automated installer to deploy Red HatOpenShift at customer site.

Question: What would happen if a customer deletes the IBM Storage Fusion HCI System or IBM Storage Fusion operators from Red Hat OpenShift Container Platform console > Installed operator page?

Answer: It is not recommended to delete the operator. If you delete, then it leaves the appliance in an inconsistent mode. Contact IBM support for further assistance.

Question: Is KEDA (Kubernetes-based Event Driven Autoscaling) supported with IBM Storage Fusion HCI System?

Answer: Yes, you should be able to use KEDA on IBM Storage Fusion HCI System. In general, see the following document on using KEDA with Red Hat OpenShift, and IBM Storage Fusion HCI System is based on an Red HatOpenShift on Bare Metal cluster - https://developer.ibm.com/patterns/scaling-an-event-driven- architecture-with-kafka-on-openshift/

Question: How to configure or order IBM Storage Fusion services (Data Cataloging, Global Data Platform, Backup & Restore, Fusion Data Foundation)?

Answer: Yes, you can install IBM Storage Fusion services from the IBM Storage Fusion HCI System user interface. For the procedure to install, see Installing services.

Question: Do the AFM nodes for IBM Storage Fusion HCI System run as containers or bare metal AFM servers?

Answer: The AFM nodes are compute nodes in the Red Hat OpenShift cluster that host the containers running the code that implements AFM. For more information about how IBM Storage Scale handles AFM, see Sharing data.

Question: Does IBM Storage Fusion HCI System support the usage of NFS protocol RWM protection in 3-site configuration?

Answer: IBM Storage Scale AFM DR does not support 3-site configuration. You can configure IBM Storage Scale stretch cluster with three copies if you have low latency networks available between three sites. Alternatively, you can configure two sites by using IBM Storage Scale Stretch cluster configuration over low latency network and configure AFM-DR over NFS RWX for the 3rd site.

Question: If the GPU enhanced nodes are not sufficient, then is there another option apart from acquiring another IBM Storage Fusion HCI System appliance? (Like adding GPU worker nodes outside the IBM Storage Fusion HCI System rack?)

Answer: No.
But you can have multiple IBM Storage Fusion HCI System appliances having Red Hat OpenShift Clusters. You can then manage these two OpenShift Container Platform clusters using Red Hat Advanced Cluster Manager.

Question: IBM Visual Insights will run on Maximo Red Hat OpenShift Container Platform instead of IBM Power but it requires GPU. Will IBM Storage Fusion HCI System include GPUs?

Answer: IBM Storage Fusion HCI System can be ordered with 6 NVIDIA A100 GPUs. If required, you can order another 2 GPU units.

Question: What to do if we see a red icon for some of the widgets in the IBM Storage Fusion HCI System infrastructure overview user interface page?

Answer: The red icon indicates a problem with that component and it needs attention. Refer to the widget page or to the events page for further details. For more information about infrastructure overview and events, see Monitoring hardware from IBM Storage Fusion HCI System user interface and Analyzing events in IBM Storage Fusion HCI System. If the problem persists, then contact IBM support for assistance.

Question: On top of the embedded Prometheus monitoring, can the user go further with monitoring integration of their systems. Can they use Alert manager to extract data and send it to an external monitoring tools? Which other options are available to centralize the IBM Storage Fusion HCI System appliance on a standard customer monitoring platform?

Answer: For every metric that is seen in Prometheus, you can configure the OpenShift alert manager to create alerts and send them to destinations supported by alert manager. As IBM Storage Fusion feeds events into OpenShift event manager, they show up in any integration that you use to monitor OpenShift events. For more information, see Monitoring and logging by using any monitoring tool.

Question: What configurations are available for IBM Storage Fusion HCI System? Can the hardware be ordered in different configurations? Can the hardware be upgraded in the field?

Answer: Yes, the hardware can be upgraded in the field. For more information about upgrade, see Upgrading node firmware and Upgrading switch firmware.
The base and minimal configuration consists of a 42u rack, dual TORs, dual management switches, and 6 dual-socket servers each populated with two 7.62 TB NVMe drives.
64 core servers with 1024GB of RAM are also available for the base.

Question: What are the minimum and maximum number of nodes?

Answer: This procedure installs and configures all the default nodes (Three controllers and three compute nodes). If you ordered additional nodes, then they get installed as well. The maximum number of servers in a rack is 18 (16 + 2 AFM nodes) and the minimum is 6 nodes.

Question: Can two IBM Storage Fusion HCI System racks be clustered in an active-active configuration?

Answer: We are calling this configuration ‘Metro sync DR’. To achieve synchronous replication between the racks, the racks must reside within a metropolitan area (for low latency) and must be connected by a high-bandwidth, high-quality network link. For the exact specification, see Metro-DR for IBM Storage Fusion HCI System.

Question: Can three IBM Storage Fusion HCI System racks be clustered in a multi-zone configuration? What are the RPO characteristics?

Answer: We are calling this configuration as ‘High-availability cluster’, also known as AFM DR in the IBM Storage Scale community. The Recovery Point Objective (RPO) depends on several factors: the latency and bandwidth of the link connecting racks across zones as well as the size and quantity of the transactions that need to be replicated.

Question: Is IBM Spectrum® Storage Scale Erasure Code Edition (ECE) deployed as a container?

Answer: Yes. IBM Storage Scale Erasure Code Edition (ECE) is deployed container native and managed through an operator.

Question: Can IBM Storage Fusion HCI System support traditional VMs and containers on the same system?

Answer: Yes, IBM Storage Fusion HCI System can support running containers and VMs is side-by-side on the same system with Red Hat OpenShift Virtualization. OpenShift Virtualization comes with Red Hat OpenShift Container Platform.
Note: The OpenShift Virtualization is a technology based on KubeVirt.

Question: Can user run content from Red Hat Marketplace on IBM Storage Fusion HCI System?

Answer: Yes, user can run content from Red Hat Marketplace on IBM Storage Fusion HCI System.

Question: What Cloud Paks will run on IBM Storage Fusion HCI System?

Answer: For existing Cloud Pak support, see IBM Cloud Paks support for IBM Storage Fusion.

Question: Can IBM Storage Fusion HCI System support Windows?

Answer: Yes, IBM Storage Fusion HCI System can support both Windows and Linux virtual machines with Red Hat OpenShift Virtualization (Virtue).

Question: Is support available for "protocol"?

Answer: Protocol is the ability to access data in IBM Storage Scale via a mechanism other than native Scale. The IBM Storage Scale supports NFS and SMB.

Question: If a IBM Storage Fusion HCI System deployed spans 3 racks, then can the control nodes be deployment across the 3 OpenShift Container Platform clusters?

Answer: When the 3 racks are initially setup, all control nodes are in the first rack (basically, you set up and configure the first rack,and then add the other two). After the initial installation is complete, control nodes can be dispersed over 3 racks.
In HA, control nodes are placed across the three racks. In expansion, the control nodes remain in one rack. The reason because the cluster is already created and you cannot change the control nodes. In expansion rack, the control nodes remain in one rack because the cluster is already created and you cannot change the control nodes.

Question: Can IBM Storage Fusion HCI System be used to expand an existing cluster?

Answer: If you use an existing HCI rack, then the new rack can be extended with an existing OpenShift Container Platform cluster. It is called the expansion rack.

Question: Do we support single OpenShift Container Platform cluster across multiple IBM Storage Fusion HCI System racks? 

Answer: Although there are restrictions, you can cluster 3 racks together in one big OpenShift Container Platform cluster.

Question: What is the minimum size of the Client environment? (3/4 x86 bare servers dedicated to containers)?

Answer: The minimum size of a IBM Storage Fusion HCI System is currently 6 nodes in a rack. The rack can scale up to 16 nodes, and 3 racks can be interconnected.

Question: What is the max power draw and cooling figures for IBM Storage Fusion HCI System especially with the newly announced hardware? 

Answer: Use the StorM tool to calculate the power consumption of a particular configuration.

Question: Is mixing of 9155-C01 / 9155-C05 compute nodes supported (for example: 3 x 32 core servers + 3 x 64 cores servers)? Also, in StorM is there a possibility to choose only one GPU server or only one AFM server? Is this correct or is a bug from tool (Initially, the option was 0 or two of them)?

Answer: Yes, mixing of 9155-C01 / 9155-C05 servers, as well as all the 9155-C00/C01/C04/C05 servers are allowed. The only server requirement is a 3x 9155-C01 or 9155-C05 Compute Node servers and 3x 9155-C01 or 9155-C05 Storage servers are needed (base minimum requirement). All servers, including GPU & AFM, can be purchased in increments of one after the base min server requirement (noted above) has been met.

Question: Can I add an expansion rack to an existing IBM Storage Fusion HCI System rack? 

Answer: Yes, you can add a new rack to an existing rack using multi-rack capability.

Question: Can I deploy more than one rack in single IBM Storage Fusion HCI System cluster?

Answer: Yes, you can deploy two or three racks as a single cluster IBM Storage Fusion HCI System using a multi-rack set up.

