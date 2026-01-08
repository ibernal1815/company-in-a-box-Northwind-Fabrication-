# Backups And Recovery

## Backup target

- Server: BKP01
- Storage: Dedicated virtual disk

## Backup scope

- Active Directory related data
- File share data on FS01
- Key configuration exports

## Schedule

- Daily incremental backups
- Weekly full backups

## Recovery testing

Restore tests include:
- Restoring a deleted file
- Recovering a configuration export

Recovery steps and results are documented after each test.
