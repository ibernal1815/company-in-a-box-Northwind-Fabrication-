# FS01 Build

## Purpose

FS01 provides centralized file services for all departments. It hosts departmental file shares secured through Active Directory security groups.

## Prerequisites

- DC01 operational and reachable
- Active Directory domain northwind.local available
- Windows Server 2022 Standard ISO available

## Virtual machine configuration

- VM name: FS01
- Operating system: Windows Server 2022 Standard
- vCPU: 2
- Memory: 8 GB
- OS disk: 80 GB
- Data disk: 150 GB
- Network adapter: VMnet10

## Network configuration

- IP address: 10.10.10.20
- Subnet mask: 255.255.255.0
- Default gateway: 10.10.10.1
- DNS server: 10.10.10.10

## Operating system configuration

- Computer name: FS01
- Time zone: Pacific Time
- Joined to domain: northwind.local
- Windows updates installed before role configuration

## Role installation

- File and Storage Services
- File Server role

## Storage configuration

- Data disk initialized and formatted as NTFS
- Volume mounted as drive F:

## Share configuration

Create the following shares on the data volume:
- Engineering
- HR
- Finance
- Sales
- Public

## Permissions

- Departmental shares grant read and write access to corresponding security groups
- Public share grants read access to all authenticated users
- Share permissions remain simple, NTFS permissions enforce access

## Validation

- Users can access assigned shares
- Unauthorized users are denied access
- File creation and modification function as expected

## Notes

FS01 does not host user profiles or roaming data.
