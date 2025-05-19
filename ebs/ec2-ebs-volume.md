# EBS Volume

EBS (Elastic Block Store) Volume is a network drive that can be attached to instances while they run. This allows instances to persist data, even after their termination. They can only be mounted to one instance at a time (at CCP level) and are bound to a specific Availability Zone (AZ). Think of them as a network USB stick.

## EBS Snapshots

EBS Snapshots allow you to make a backup (snapshot) of your EBS volume at a specific point in time. It's not necessary to detach the volume to do a snapshot, but it's recommended. Snapshots can be copied across AZs or Regions.

## EBS Snapshot Archive

EBS Snapshot Archive allows you to move a Snapshot to an "archive tier" that is 75% cheaper. It takes between 24 to 72 hours to restore the archive.

## Recycle Bin for EBS Snapshots

Recycle Bin for EBS Snapshots allows you to set up rules to retain deleted snapshots so you can recover them after an accidental deletion. You can specify the retention period, which can range from 1 day to 1 year.

## Fast Snapshot Restore (FSR)

Fast Snapshot Restore (FSR) forces full initialization of a snapshot to eliminate latency on the first use.

## EBS multi-attach - io1/io2 family

Attach the same EBS volume to multiple EC2 instances in the same AZ
Each instance has full read & write permissions to high-performance volume. Up to 16 EC2 instances at a time, must use a file system that's cluster-aware

### Use case: 
- Achieve higher application availability in clustered Linux applications
- Applications must manage concurrent write operations

## EBS encryption

When you create an encrypted EBS volume, get the following:
- Data at rest is encrypted inside the volume
- All the data in flight moving between the instance and the volume is encrypted
- All snapshots are encrypted
- All volumes create from the snapshots

Encryption and decryption are handled transparently (you have nothing to do). Encryption has a minimal impact on latency, EBS Encryption leverages keys from KMS (AES-256). Copying an unencrypted snapshot allows encryption. Snapshots of encrypted volumes are encrypted

