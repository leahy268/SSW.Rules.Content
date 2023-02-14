---
type: rule
title: Do you make sure there is a valid backup?
uri: is-there-a-valid-backup
authors:
  - title: Warwick Leahy
    url: www.ssw.com.au/people/warwick-leahy
created: 2023-02-12T22:41:58.610Z
guid: 93ee99b8-e566-4455-b122-588e4fd48122
---
It is crucial to verify that all clients have a reliable backup solution in place. This helps ensure the safety and availability of their critical data in the event of an unexpected disaster or loss.  This should be documented so that when a new person joins a project they can quickly see how the backup is performed. 

If a client just tells you that they are handling the backups document the decision on the project so that someone new understands.  However this should still be discussed as they may not completely understand.

<!--endintro-->



### What type of Backup?

This depends a lot on what needs to be backed up.

- Azure storage and VM's - [Azure Backup](https://learn.microsoft.com/en-us/azure/backup/backup-overview) provides excellent backup for any VM's or storage, restoring data and vm's is almost instant.
- Azure SQL - [Azure SQL Built-in Backup](https://learn.microsoft.com/en-us/azure/backup/backup-azure-sql-database) - Use a SKU that allows long enough retention periods and choosing which point to restore 
- Office365/SharePoint - A product like [N-Able Cove Data Protection](https://www.n-able.com/products/cove-data-protection) provides 7 years of retention and 1Tb of storage per user
- On-Premises Servers and VM's - Azure Backup can be used to back up on-premises servers and VMs with sufficient bandwidth. Alternatively, local backup can be achieved through [Microsoft Data Protection Manager](https://learn.microsoft.com/en-us/system-center/dpm/dpm-overview?view=sc-dpm-2022), which offers excellent functionality. 

### Testing backups




It is important to regularly test backups to ensure that they are successful and the data can be recovered in the event of an emergency. Regular communication with clients about their backup solution and regularly scheduled testing will help ensure their data remains secure.

### Project Handover

Once a project is ready for production, backups should be discussed with the client and they should be comfortable with the process as well as any retention periods for the backups.