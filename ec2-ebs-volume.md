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