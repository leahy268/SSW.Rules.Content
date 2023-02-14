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

<!--endintro-->

If a client just tells you that they are handling the backups document the decision on the project so that someone new understands.



### What type of Backup?

This depends a lot on what needs to be backed up.

- Azure storage and VM's - Use Azure Backup https://learn.microsoft.com/en-us/azure/backup/backup-overview
- Azure SQL - Use a SKU that extends the backup and use the built-in backup https://learn.microsoft.com/en-us/azure/backup/backup-azure-sql-database
- Office365/SharePoint - A product like N-Able Cove Data Protection https://www.n-able.com/products/cove-data-protection provides 7 years of retention and 1Tb of storage per user
- On-Premises Servers and VM's - With enough bandwidth these can be backed up using Azure Backup, or without Microsoft Data Protection Manager provides excellent local backup https://learn.microsoft.com/en-us/system-center/dpm/dpm-overview?view=sc-dpm-2022

### Testing backups




It is important to regularly test backups to ensure that they are successful and the data can be recovered in the event of an emergency. Regular communication with clients about their backup solution and regularly scheduled testing will help ensure their data remains secure.

### Project Handover

Once a project is ready for production, backups should be discussed with the client and they should be comfortable with the process and retention periods of backups.