---
layout: page_collection
title: Step 3 - Develop a Deployment Schedule
permalink: 3_step-3
---
<script>
$(function() {
  $( "#accordion" ).accordion({
    heightStyle: "content",
    collapsible: "true",
    active: "false"
  });
  $( "#accordion_2" ).accordion({
    heightStyle: "content",
    collapsible: "true",
    active: "false"
  });
});
</script>

<script src="https://use.fontawesome.com/e20c671b68.js"></script>
------------------------------------------------------------------

LACS deployments are complex undertakings and therefore require significant up-front planning to ensure a successful deployment. Program/project managers should consider following a structured life cycle model to assist them with the planning process. This section introduces a phased model that identifies key activities during a LACS development. The five phases are: Planning, Requirements and Design, Build, Implement, and Operate and Maintain. This section examines each of the phases and discusses the LACS-specific events that should occur as part of each phase.

<br>

<div style="background-color: #edf1f3;color: black;margin: 10px;padding: 10px">

<h3><span>Privacy Tip</span></h3>
<p><span>Involve representatives from your agency's Privacy Office during the Requirements and Design and Build phases to ensure that solutions are designed in a manner that protects privacy. While many privacy activities typically occur during the Requirements and Design and Build phases, you should also consider data protection and privacy requirements throughout the entire LACS development life cycle and incorporate appropriate privacy measures. Privacy shouldn't be overlooked when attempting to solve complex technical challenges, as the overarching goal of increased efficiency and security needs to be maintained.</span></p>

</div>

<br>

<div id="accordion" markdown="1">

### Planning Phase
<div markdown="1">

The Planning Phase is the first step in beginning a LACS effort. Completing the Planning Phase is critical for modernizing LACS solutions, as many of the common problems encountered can be avoided through careful planning. The table below provides a list of common activities that should occur during the Planning Phase.

<br>

| <center> Activity </center> | <center> Description </center> |
|-----------------------------|--------------------------------|
| Conduct Cost/Benefit Analysis | Evaluate the factors discussed in the Program Funding section and conduct a cost/benefit analysis to determine an appropriate LACS solution |
| Develop LACS Business Plan | Develop a business plan to support the improvement of the existing LACS infrastructure. This should lay out the selected approach, timeline, resource requirements, and estimated costs. |
| Develop Implementation Plan/Schedule | Develop a phased implementation approach and schedule based on available information using standardized agency resources. This should include planning for future integration periods beyond the initial LACS deployment |
| Categorize the LACS | Conduct <a href="http://csrc.nist.gov/groups/SMA/fisma/Risk-Management-Framework/categorize/index.html" target="_blank"> Step 1 of the Risk Management Framework (RMF): Categorize Information Systems </a> based on mission/business objectives. Register the LACS in the agency’s IT system inventory|
| Begin Application Prioritization | Examine IT resources and develop application assessment criteria in order to prioritize/organize deployment of LACS services to agency IT resources |
| Develop Risk Management Plan | Use existing risk management sources to develop  a Risk Management Plan for handling risks related to deploying LACS |
| Develop Communications Plan | Develop the approach and plan to communicate (using a variety of media) the changes that a LACS effort will bring to internal users, resource owners, and stakeholders |
| Develop Application Integration Guide | Develop an Application Integration Guide, a formal document used to outline the process that an agency’s IT resources will go through to become integrated with the LACS solution |
| Develop LACS Migration Plan | Develop a migration plan that outlines how the agency plans to transition its logical resources to use the access control system |
| Develop Pilot Implementation Plan | Develop a plan and schedule for piloting the LACS solution on a small subset of the user population with well-defined resource requirements |

</div>

### Requirements and Design Phase
<div markdown="1">

Once your agency has planned its LACS effort, you should thoroughly documents the requirements for the LACS solution and define how the solution should operate within the agency‘s infrastructure. The table below provides a list of common activities that should occur during the Requirements and Design Phase.

<br>

| <center> Activity </center> | <center> Description </center> |
|-----------------------------|--------------------------------|
|  Finalize LACS Solution Requirements  | Conduct a requirements gathering exercise with stakeholders and impacted parties at all organizational levels to document requirements of the LACS solution. These requirements are critical as they will be used to design, build, and configure the LACS capability. |
|  Validate LACS Solution Requirements | Validate the documented requirements with the LACS stakeholders in order to ensure that the LACS solution is properly designed and configured to meet your agency’s needs|
|  Identify and Secure Funding Sources  | Use the LACS business plan to secure funding sources for the LACS effort. All information technology (IT) investments need to include funding as appropriate to support ICAM activities. |
|  Select Security Controls  | Conduct <a href="http://csrc.nist.gov/groups/SMA/fisma/Risk-Management-Framework/select/index.html" target="_blank"> Step 2 </a> of the Risk Management Framework (RMF): Select Security Controls by choosing the appropriate security controls and documenting the selected controls in the security plan |
|  Develop Solution Architecture  | Develop an initial solution architecture for the LACS implementation, which defines the solution components and describes their interactions |
|  Identify Authoritative Stores  | Identify the authoritative store(s) of user information that will be used with LACS solution to enable automated provisioning of user accounts |
|  Establish Common Rules, Roles, and Policies | Determine the common roles, rules, and policies that will apply to all applications in the enterprise environment. These common rules serve as a base set of configurable items within a LACS solution, and added granularity can be provided on a per application basis. |
|  Map Consolidated Rules, Roles, and Policies to Applications | Map the base set of rules, roles, and policies to those currently used by the target applications (e.g., the downstream IT resources being protected by the LACS infrastructure) |
|  Document System Design  | Draft an initial system design document that clearly states how the system should function within the agency’s environment. The document should demonstrate how common roles, rules, and policies will be applied to enterprise LACS applications, and will further demonstrate how granular level policies, rules, and roles are supported to meet the LACS application owner needs. |
|  Document LACS Use Cases  | Document detailed LACS use cases, which the designed solution should address in the build phase. These models should seek to capture existing manual processes that will be automated, along with any exception workflows that are not part of the primary workflow. |
|  Define and Configure Provisioning Workflows  | Define provisioning workflows, which are used to determine how users are granted access to logical resources and what approvals or additional steps are required. Provisioning workflows are based on a solid understanding of the enterprise approach to common rules, roles, and policies which are applied consistently across managed end-point applications. |
|  Develop Demo Application  | Consider development of a demo application that can be used for training business/resource owners on the LACS capabilities being implemented. Having such a capability provides LACS program management with the ability to showcase all the capabilities and streamline integration processes. |
|  Determine Physical Deployed Architecture | Outline the physical elements that need to reside in data centers, and allow for advanced coordination of the end state solution that will need to be located/hosted there. You should include the production environment, pre-production testing environment, user acceptance testing environment, and the development testing environment. These four environments will need to be maintained throughout a solution life cycle to allow for proper testing, regression testing, and solution integration over time. |
|  Conduct Detailed Application Assessments  | As part of the application prioritization and integration process, conduct application assessments as a means of gaining information about resource configuration and existing workflows |
|  Conduct Privacy Assessment  | Review the LACS design and solution requirements against established privacy guidelines and agency policies to ensure compliance |
|  Conduct Resource Acquisition  | With funding sources secured, conduct the process of purchasing any required hardware, software, or labor support that will be needed |

</div>

### Build Phase
<div markdown="1">

Following the Design Phase, agencies enter the Build Phase, where the majority of the technical solution development, configuration, and testing occurs. The table provides a list of common activities that should occur during the Build Phase.

<br>

| <center> Activity </center> | <center> Description </center> |
|-----------------------------|--------------------------------|
|  Stand Up Development and Test Environments  | Establish development and testing environments so that LACS developers and testers can conduct build activities in an environment that does not impact the agency’s production systems |
|  Build/Configure Servers  | Build and/or configure servers to properly operate the LACS solution, as needed based upon the chosen implementation path. Ensure that hardware is on-hand in an appropriate timeframe |
|  Install Supporting Software  | Install supporting software (i.e., Commercial Off-The-Shelf [COTS] Identity Access Management [IAM] Suite) on LACS servers, as needed based upon the chosen implementation path |
|  Configure Supporting Software  | Configure LACS software to specifically meet your agency’s unique needs and/or perform certain functions, as needed based upon the chosen implementation path |
|  Implement and Assess Security Controls  | Conduct Steps 3 and 4 of the <a href="http://csrc.nist.gov/groups/SMA/fisma/framework.html" target="_blank">  Risk Management Framework (RMF) </a> by applying the controls identified in the requirements and design phase and by assessing the adequacy and effectiveness of the security controls and documenting the findings in an assessment report |
|  Build Resource Adapters, Service Interfaces, and Network Connectors  | Build and configure network connectors, service interfaces, and resource adapters in order to deploy the LACS solution onto your agency’s network and integrate with IT resources |
|  Develop a Test Plan and Test Scripts  | Define a test plan and test scripts to organize the testing process and identify the key capabilities that must occur successfully to ensure that the LACS solution performs as it was designed and operates securely and efficiently |
|  Conduct Testing on Initial Build  | Perform testing (including failover and regression testing, interoperability testing with other infrastructure components, and performance testing) on the LACS solution to ensure that system errors are found and corrected before the solution is deployed |
|  Conduct Pilot Implementation Deployment  | Conduct a pilot implementation to expose a small subset of your agency's user base to the LACS solution for the purpose of evaluating the solution’s operations against real-world requirements |

</div>

### Implement Phase
<div markdown="1">

Once your agency has configured its LACS solution and tested to ensure that it meets agency requirements and performs appropriately, the project enters the Implement Phase. This phase consists of activities for migrating the LACS solution from a development and test environment into the agency‘s production infrastructure. The table below provides a list of common activities that should occur during the Implement Phase.

<br>

| <center> Activity </center> | <center> Description </center> |
|-----------------------------|--------------------------------|
|  Authorize the LACS  | Conduct Step 5 of the <a href="http://csrc.nist.gov/groups/SMA/fisma/framework.html" target="_blank">  Risk Management Framework (RMF) </a> Risk Management Framework (RMF):  Authorize Information System </a> by preparing and submitting the security authorization package to the authorizing official. The authorizing official chooses to accept the risk and authorize the system if the risk associated with operating the LACS is deemed acceptable. |
|  Conduct User Acceptance Testing  | Conduct user acceptance testing to ensure that the LACS solution is acceptable to stakeholders and end users and performs the required functions in an appropriate manner |
|  Deploy LACS Solution to Live Production Environment  | Deploy the LACS solution on your agency’s network infrastructure and begin controlling access to protected resources |
|  Conduct User Training  | Develop training materials and conduct user training prior to LACS deployment to ensure that users can access their worksites without disruption |
|  Perform Awareness and Outreach  | Conduct awareness and outreach activities in accordance with the Communications Plan developed as part of the Planning Phase. This involves actively communicating to users that a new access control system is being deployed, the benefits and efficiencies that users can expect, and any steps necessary to begin using the new system. |

</div>

### Operate and Maintain  Phase
<div markdown="1">

After your LACS solution has been deployed, the project enters the Operate and Maintain Phase. This phase lasts for the remainder of the time that the LACS solution is in use and consists of ongoing management and system maintenance activities such as conducting training, operating the LACS solution, and protecting new resources as they are integrated with the enterprise solution. The table below provides a list of common activities that should occur during the Operate and Maintain Phase.

<br>

| <center> Activity </center> | <center> Description </center> |
|-----------------------------|--------------------------------|
|  Monitor Security Controls  | Conduct <a href="http://csrc.nist.gov/groups/SMA/fisma/Risk-Management-Framework/monitor/index.html" target="_blank"> Step 6 </a> of the Risk Management Framework (RMF): Monitor Security Controls by monitoring changes to the information system and its environment of operation and conducting ongoing assessments of security controls in accordance with the monitoring strategy |
|  Ongoing User Training  | Continue to update and modify user training curriculums as the LACS solution matures, new resources are protected, and new users are added. Conduct additional training as necessary. |
|  Execute Change Control Board (CCB)  | Conduct activities with the CCB to evaluate potential changes to the LACS solution and provide a governance structure for determining which solution changes should be implemented. |
|  Build/Configure Resource Adapters and Service Interfaces  | Build/configure additional resource adapters and service interfaces to properly connect and manage authentication to new applications as they are integrated into the LACS infrastructure. |
|  Modify Provisioning Workflows  | Update provisioning workflows as business needs and access rules change over time. Changes may also be required as resource owners experience the benefits that can be provided by LACS services and provisioning workflows can be streamlined. |
|  Conduct Hardware/ Technology Refresh  | Conduct periodic updates and/or upgrades to solution hardware and other technology over the lifespan of a LACS solution as a means of extending the usable life of the solution or adding new capabilities. |
|  Remove Sunsetted Resources  | IT resources are replaced, upgraded, or consolidated over time as mission and business needs change. Accordingly, as applications become sunsetted, user privileges will need to be de-provisioned and the resource itself can be disconnected from the LACS solution. |

</div>













