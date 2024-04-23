# Enterprise-Troubleshooting-Environment For Image Deployment
<div style="text-align:center;">
![image](https://github.com/AngelPerales10/Enterprise-Troubleshooting-Environment/assets/108242721/60c882b5-1f4e-4ef1-935e-3a3abe48d322) 
</div>
**Author:** Angel Perales

## Table of Contents

- [Summary](#summary)
- [Review of Other Work](#review-of-other-work)
- [Changes to the Project Environment](#changes-to-the-project-environment)
- [Methodology](#methodology)
- [Project Goals and Objectives](#project-goals-and-objectives)
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


## Conclusions

The project successfully automated credential caching, streamlining IT support operations. Immediate impacts include a more streamlined deployment process and a reduction in manual errors and time. Long-term impacts include enhanced user experience and continued operational efficiency.

## Project Deliverables

### Virtualized Lab Environment
- Documentation outlining setup, configuration, and functionality.

![image](https://github.com/AngelPerales10/Enterprise-Troubleshooting-Environment/assets/108242721/60c882b5-1f4e-4ef1-935e-3a3abe48d322)


### Configurations and Scripts
- Final PowerShell script developed for credential caching.
- It holds the support credentials as variables, and opens up the application Notepad as the credentialed user.
- That user connects to Active Directory to verify itself as a user of the domain, and opens Notepad as that user, only for that one action. This in itself caches the user onto the laptop.
- Actual credentials have been changed due to obvious security reasons.
- We chose this script out of the many other winners due to its basic nature and unintrusive actions on the operating systems configurations.

`$username = "domain\itsupport"
$password = "password" | ConvertTo-SecureString -AsPlainText -Force
$creds = New-Object System.Management.Automation.PSCredential($username, $password)
Start-Process "notepad.exe" -Credential $creds -LoadUserProfile
`

### Integrated Caching Script into Production
- The script that is marked as a deliverable above has now been added to our deployment process.
- It has not been added directly into the deployment software, rather, it has been added to the end of the cleanup process script that runs at the end of every deployment.
- A visual deliverable cannot be added to this repository as I am not permitted to take screenshots from our production machine.

### Efficient Testing Environment
- Established lab that will be used to test future deployment issues / configurations.

![image](https://github.com/AngelPerales10/Enterprise-Troubleshooting-Environment/assets/108242721/e5ce8c54-3ec6-432b-bf79-54ec12f23454)


### Automated Deployment Process
- Removing manual step from deployment, saving about 15 minutes of manual work per deployment

![image](https://github.com/AngelPerales10/Enterprise-Troubleshooting-Environment/assets/108242721/7e870575-f92c-48e6-b6b2-4997aaa9fc7f)


## References
BTNHD. (2019, January 28). MDT 8456 (step-by-step) BASIC INSTALLATION GUIDE!. [YouTube.](https://www.youtube.com/watch?v=yIOotj2V118)

Deland-Han. (n.d.). Configure windows to Automate Logon - Windows Server. Configure Windows to automate logon - Windows Server | [Microsoft Learn.](https://learn.microsoft.com/en-us/troubleshoot/windows-server/user-profiles-and-logon/turn-on-automatic-logon)

BalaDelli. (n.d.-a). Toolkit reference - microsoft deployment toolkit (MDT) scripts - microsoft deployment toolkit. Toolkit reference - Microsoft Deployment Toolkit (MDT) Scripts - Microsoft Deployment Toolkit | [Microsoft Learn.](https://learn.microsoft.com/en-us/mem/configmgr/mdt/scripts)

