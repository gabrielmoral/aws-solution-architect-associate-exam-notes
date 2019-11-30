#### Storage gateway

It is a service that connects on-premises software appliance with cloud-based storage. The services enables to store data in the cloud securely.

It is a virtual or physical device.

3 flavours:

**File Gateway (NFS & SMB)**

Files are stored as objects in your S3 buckets.

**Volume Gateway (iSCSI)**

It is a way to store your virtual hard disk drives in the cloud.

- Stored Volumes
  The entire dataset is stored locally and asynchronous backs up the data in S3.
- Cached Volumes
  Entire dataset is stored in S3 and the most frequent data is kept locally.

**Tape Gateway**

You can replace your entire tapes collection to the cloud using tape gateway.