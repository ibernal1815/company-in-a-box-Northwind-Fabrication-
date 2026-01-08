# BKP01 Build

## Purpose

BKP01 serves as the centralized backup repository for critical systems and data. It supports recovery testing and validation.

## Prerequisites

- Network connectivity to Server Network
- Ubuntu Server ISO available
- Backup scope defined

## Virtual machine configuration

- VM name: BKP01
- Operating system: Ubuntu Server LTS
- vCPU: 2
- Memory: 4 GB
- Disk: 150 GB
- Network adapter: VMnet10

## Network configuration

- IP address: 10.10.10.40
- Subnet mask: 255.255.255.0
- Default gateway: 10.10.10.1
- DNS server: 10.10.10.10

## Operating system configuration

- Hostname: BKP01
- Time zone: Pacific Time
- Automatic security updates enabled

## Backup configuration

- Backup storage isolated from production services
- Backups received from DC01 and FS01
- Configuration exports included in backup scope

## Schedule

- Daily incremental backups
- Weekly full backups

## Recovery testing

- File restore tests performed periodically
- Results documented after each test

## Notes

BKP01 does not host production services.
