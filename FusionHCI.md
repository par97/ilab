IBM Fusion HCI system provides a fully integrated, turnkey platform for running and maintaining all of your on-premises Red Hat OpenShift applications.
It provides data services like Global Data Platform and Fusion Data Foundation. It also provides data backup and restore services.

IBM Storage Fusion Data Foundation is a highly integrated collection of cloud storage and data services for Red Hat OpenShift Container Platform. It is available as part of the Red Hat OpenShift Container Platform service catalog, packaged as an operator to facilitate simple deployment and management.

Fusion Data Foundation services are primarily made available to applications in the form of storage classes that represent the following components:
1.Block storage devices, catering primarily to database workloads, for example, Red Hat OpenShift Container Platform logging and monitoring, and PostgreSQL.
2.Shared and distributed file system, catering primarily to software development, messaging, and data aggregation workloads, for example, Jenkins build sources and artifacts, Wordpress uploaded content, Red Hat OpenShift Container Platform registry, and messaging using JBoss AMQ.
3.Multicloud object storage, featuring a lightweight S3 API endpoint that can abstract the storage and retrieval of data from multiple cloud object stores.
4.On-premises object storage, featuring a robust S3 API endpoint that scales to tens of petabytes and billions of objects, primarily targeting data intensive applications, for example, the storage and access of row, columnar, and semi-structured data with applications like Spark, Presto, Red Hat AMQ Streams (Kafka), and even machine learning frameworks like TensorFlow and Pytorch.

Fusion Data Foundation version 4.x integrates a collection of software projects, including:
1.Ceph, providing block storage, a shared and distributed file system, and on-premises object storage.
2.Ceph CSI, to manage provisioning and lifecycle of persistent volumes and claims.
3.NooBaa, providing a Multicloud Object Gateway (MCG).
4.Fusion Data Foundation, rook-ceph, and NooBaa operators to initialize and manage Fusion Data Foundation services.
