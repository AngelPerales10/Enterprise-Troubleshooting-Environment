# Enterprise-Troubleshooting-Environment For Image Deployment

**Author:** Angel Perales Jr.  

## Table of Contents

- [Summary](#summary)
- [Review of Other Work](#review-of-other-work)
- [Changes to the Project Environment](#changes-to-the-project-environment)
- [Methodology](#methodology)
- [Project Goals and Objectives](#project-goals-and-objectives)
- [Project Timeline](#project-timeline)
- [Unanticipated Requirements](#unanticipated-requirements)
- [Conclusions](#conclusions)
- [Project Deliverables](#project-deliverables)
- [References](#references)

## Summary

The Enterprise Troubleshooting Image Deployment Lab project aimed to address critical issues within the organization's deployment infrastructure. By creating a testing environment, the project enabled safe and efficient troubleshooting without disruptions to the production environment. The project involved thorough planning, virtualization, analysis, design, implementation, testing, and maintenance phases.

## Review of Other Work

### MDT 8456 (Step-by-Step) Basic Installation Guide!
- **Provider:** BTNHD
- **Description:** Instructional video providing insights into installing MDT, including configuring roles like WDS for network booting and deployment.
- **Impact:** Contributed to setting up the testing lab environment and configuring image deployment solutions.

### Turn on automatic logon in Windows
- **Provider:** Microsoft
- **Description:** Documentation on configuring automatic logon in Windows systems.
- **Impact:** Initial basis for testing, though not implemented due to security risks.

### Microsoft Deployment Toolkit (MDT) Documentation – References – Scripts
- **Provider:** Microsoft
- **Description:** Documentation on LTICleanup.wsf script, crucial for post-deployment cleanup.
- **Impact:** Identified issues with LTICleanup.wsf through deployment logs, aiding in troubleshooting.

## Changes to the Project Environment

The project introduced a dedicated testing environment, enhancing security and minimizing disruptions. By ensuring IT support credentials are cached onto imaged laptops during deployment, remote support capability was significantly improved.

## Methodology

The Systems Development Life Cycle (SDLC) was followed, ensuring a structured approach. Phases included planning, analysis, design, implementation, testing, and maintenance.

## Project Goals and Objectives

### Goal 1: Solve issue with caching IT support credentials
- **Objective 1:** Create a testing environment
- **Objective 2:** Test different configurations and scripts
- **Objective 3:** Develop and integrate caching script into production

### Goal 2: Streamline troubleshooting processes
- **Objective 1:** Establish testing environment
- **Objective 2:** Automate deployment configurations

## Project Timeline

Detailed project timeline with milestones and durations.

## Unanticipated Requirements

Outlined unanticipated technical and learning curve requirements encountered during the project.

## Conclusions

The project successfully automated credential caching, streamlining IT support operations. Immediate impacts include a more streamlined deployment process and a reduction in manual errors and time. Long-term impacts include enhanced user experience and continued operational efficiency.

## Project Deliverables

### Virtualized Lab Environment
- Documentation outlining setup, configuration, and functionality.

### Configurations and Scripts
- Final PowerShell script developed for credential caching.

### Integrated Caching Script into Production
- Description of integrating the caching script into the deployment process.

### Efficient Testing Environment
- Description of the testing environment and its utility.

### Automated Deployment Process
- Overview of the streamlined deployment process.

## References

List of references used in the project.
