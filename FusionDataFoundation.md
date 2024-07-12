IBM Storage Fusion Data Foundation is software-defined storage that is optimized for container environments. It runs as an operator on OpenShift Container Platform to provide highly integrated and simplified persistent storage management for containers.

IBM Storage Fusion Data Foundation is a rebranded product from Redhat OpenShift Data Foundation, available since version Fusion Data Foundation 4.12. IBM Storage Fusion Data Foundation is functionally equal to Redhat Openshift Data Foundation, since they share the same code base.

Fusion Data Foundation services are primarily made available to applications in the form of storage classes that represent the following components:
- Block storage devices, catering primarily to database workloads.
- Shared and distributed file system, catering primarily to software development, messaging, and data aggregation workloads.
- Multicloud object storage, featuring a lightweight S3 API endpoint that can abstract the storage and retrieval of data from multiple cloud object stores.
- On-premises object storage, featuring a robust S3 API endpoint that scales to tens of petabytes and billions of objects, primarily targeting data intensive applications.

Fusion Data Foundation is built on a collection of software projects, including:
- Ceph, providing block storage, a shared and distributed file system, and on-premises object storage.
- Ceph CSI, to manage provisioning and lifecycle of persistent volumes and claims.
- NooBaa, providing a Multicloud Object Gateway (MCG).
- Fusion Data Foundation, rook-ceph, and NooBaa operators to initialize and manage Fusion Data Foundation services.
  
To install Fusion Data Foundation, IBM Storage Fusion needs be installed first. Then, Fusion Data Foundation could be installed in the following way:
- Go to Services page in IBM Storage Fusion user interface.
- In the Available section, click the Data Foundation tile.
- In the Data Foundation page, go through the details about the service and click Install.
