# openstack-lab

## Overview
This project is used to track the artifacts and resources related to building a lab environment for hosting OpenStack (starting with Caracal). Some of the content was developed with the aid of [Anthropic's Claude][def-claude].
At the end of this project, my goal was to have a production-like, secure, and highly available OpenStack environment that would cover the following:
* Design a comprehensive architecture
  * Create a robust network topology with dedicated segments for management, storage, and external traffic
  * Design an efficient hardware allocation strategy maximizing the utility of each server
  * Implement redundancy at multiple levels (network bonds, RAID arrays, dual controllers)
* Implement Physical Infrastructure
  * Configure network switches with appropriate segmentation
  * Set up network bonding for high availability
  * Implement jumbo frames for storage performance
  * Configure various RAID levels appropriate to each use case
* Deploy Operating System and Base Configuration
  * Install Ubuntu 22.04 LTS on all nodes
  * Configure network interfaces and security settings
  * Set up storage systems with appropriate filesystems and mount points
  * Optimize system parameters for OpenStack workloads
* Prepare for OpenStack Deployment
  * Configure [Kolla-Ansible][def-kolla-ansible] deployment tools
  * Set up SSH key-based authentication between nodes
  * Create comprehensive deployment parameters
  * Verify all prerequisites for successful deployment
* Setup a private cloud with SSL/TLS using OpenStack Caracal
  * Deploy a full OpenStack environment using Kolla-Ansible
  * Configure and implement SSL/TLS security for OpenStack services
  * Set up multi-tier storage with different performance characteristics
  * Configure high availability for OpenStack services
  * Verify the functionality of your OpenStack deployment
  * Troubleshoot common deployment issues
  * Maintain and rotate SSL/TLS certificates

There are several artifacts in this project that outline how I built and configured this environment based on the hardware I had avaialble at this time. Mostly a hodge-podge of old servers and workstations that I have accumulated over time. Meaning that they are relatively old and slow, but are great for experimentations.

I call this experiment, the "Wolf Den" after a team I co-created and co-ran (with [Claudio Lichtenthal][def-claudio]) called the "Wolf Pack". 

Brief description of the project, its purpose, and the problem it solves.

## Architecture
High-level overview of the architecture with a link to detailed documentation.

![Physical Network Topology][def-pnt]

![Logical OpenStack Architecture][def-losa]

## Technologies Used
- OpenStack (version)
- Kolla-Ansible (version)
- Terraform (version)
- Kubernetes (version) [for K8s project]
- Other relevant technologies

## Features
- Key feature 1
- Key feature 2
- Key feature 3

## Deployment
Brief instructions for deploying the project, with links to detailed documentation.

## Challenges and Solutions
Overview of significant challenges encountered and how they were solved.

## Lessons Learned
Key insights gained from this project.

## Future Improvements
Planned or potential enhancements.

[def-claude]: https://claude.ai/new
[def-kolla-ansible]: https://docs.openstack.org/kolla-ansible/latest/
[def-claudio]: https://www.linkedin.com/in/claudio-lichtenthal-50a33a7?lipi=urn%3Ali%3Apage%3Ad_flagship3_profile_view_base_contact_details%3Bconli94pS%2BWnzzuq8pf9MQ%3D%3D
[def-pnt]: architecture/diagrams/oslpg-guide-p2d-physical-network-topology-v3.svg
[def-losa]: architecture/diagrams/oslpg-guide-p3d-logical-openstack-architecture-v3.svg
