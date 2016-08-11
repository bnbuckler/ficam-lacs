---
layout: page_collection
title: Step 4 - Build Architecture
permalink: 4_step-4
---
<script>
$(function() {
  $( "#accordion" ).accordion({
    heightStyle: "content",
    collapsible: "true",
    active: "false"
  });
});
</script>

<script src="https://use.fontawesome.com/e20c671b68.js"></script>
-----------------------------------------------------------

Following the Design Phase, agencies enter the Build Phase, where the majority of the technical solution development, configuration, and testing occurs. Activities may occur in parallel, and completion times can vary widely based on organizational size and project complexity.

## <span style="color: #0C5C89">**Checklist**</span>

> <i class="fa fa-check-square-o"></i> &nbsp;**Stand Up Development and Test Environments.** Establish development and testing environments so that LACS developers and testers can conduct build activities in an environment that does not impact the agency’s production systems.

> <i class="fa fa-check-square-o"></i> &nbsp;**Configure agency workstations to use smart cards.** Agency workstations may require additional components in order to utilize smart cards. These additional components include: 

>> * **Smart card readers.** Includes internal or external hardware components and associated device drivers necessary to access PKI certificate data stored on the smart card.

>> * **Middleware.** A software component that is required to allow communication between the smart card, smart card reader, and workstation. Some older versions of operating systems will require middleware to support PIV card use. Agencies may also want to provide middleware to support advanced card management features. Multiple middleware products, from a variety of approved vendors are available through the GSA FIPS 201 Evaluation Program Approved Products List. A third party plug-in may be necessary if the workstation OS does not natively support certain protocols.

>> * **Third party plug-ins.** A software component that may be required for workstations that run an operating system that does not support certain protocols.

> <i class="fa fa-check-square-o"></i> &nbsp;**Build/Configure Servers and Networks.** Build and/or configure servers and networks to properly operate the LACS solution, as needed based upon the chosen implementation path. Agencies should align with acquisition activities (if applicable) to ensure that hardware is on-hand in an appropriate timeframe. Visit “PIV Authentication Playbook” for detailed configuration and developer guides.

>> * **Ensure high network availability.** The network providing access to the CRLs, OCSP services, and path validation services must be highly available. Authentication of PIV cards will fail if the certificate status or trust chain for the certificate is not available. LACS components are considered high value, and should be segmented from the rest of the network. A compromise of the LACS system provides an attacker with more access to all connected resources. Components should be positioned within network segments based on a least privilege approach. CRLs, OCSP, and SCVP responders are considered public and should be in the demilitarized zone (DMZ). 

>> Access management agents and proxies should be collocated with the protected agency applications, whether on the enterprise Local Area Network (LAN), or in the DMZ. Primary LACS components (i.e., Identity Manager, Access Manager, Role Manager, Directory Server,  Federated Access  Manager,  and  Analytics  & Reporting Tool)  should   be configured in a protected subnet with access limited to only essential personnel at a network level. Additionally, networks supporting LACS components must meet NIST standards for fail-over/redundancy capabilities to ensure high availability.


> <i class="fa fa-check-square-o"></i> &nbsp;**Install Supporting Software.** Install supporting software (i.e., Commercial Off-The-Shelf [COTS] Identity Access Management [IAM] Suite) on LACS servers, as needed based upon the chosen implementation path.

> <i class="fa fa-check-square-o"></i> &nbsp;**Configure Supporting Software.** Configure LACS software to specifically meet the agency’s unique needs and/or perform certain functions, as needed based upon the chosen implementation path.


> <i class="fa fa-check-square-o"></i> &nbsp;**Implement and Assess Security** Controls. Conduct Steps 3 and 4 of the Risk Management Framework (RMF) by applying the controls identified in the requirements and design phase, assessing the adequacy and effectiveness of the security controls, and documenting the findings in an assessment report.


> <i class="fa fa-check-square-o"></i> &nbsp;**Build Resource Adapters, Service Interfaces, and Network Connectors.** Build and configure network connectors, service interfaces, and resource adapters in order to deploy the LACS solution onto the agency’s network and integrate with IT resources.


> <i class="fa fa-check-square-o"></i> &nbsp;**Develop a Test Plan and Test Scripts.** Define a test plan and test scripts to organize the testing process and identify the key capabilities that must occur to ensure that the LACS solution performs correctly, securely and efficiently.


> <i class="fa fa-check-square-o"></i> &nbsp;**Conduct Testing on Initial Build.** Perform testing (including failover and regression testing, interoperability testing with other infrastructure components, and performance testing) on the LACS solution in a development and/or test environment to ensure that system errors are found and corrected before the solution is deployed on the agency’s network.


> <i class="fa fa-check-square-o"></i> &nbsp;**Conduct Pilot Implementation Deployment.** Conduct a pilot implementation to expose a small subset of the agency’s user base to the LACS solution for the purpose of evaluating the solution’s operations against real-world requirements.

<br>

<div style="background-color: #edf1f3;color: black;margin: 10px;padding: 10px">

<h3><span>Privacy Tip</span></h3>
<p><span>While pilot implementations are often small in size and scope, agencies should keep in mind that legal and regulatory requirements for privacy and data protection apply equally to pilot implementations. Agencies should involve appropriate personnel from privacy and security offices to ensure that adequate safeguards are in place prior to implementing pilot activities.</span></p>

</div>

<br>

> When establishing a LACS pilot implementation, agencies should consider several specific factors, which influence not only the success of the pilot but may also impact the agency‘s ability to predict the success of wide-scale deployment. These factors include:

>> * **Define scope of pilot.** Start small with limited number of willing and informed users, using agency PIV cards to access the agency‘s domain. Consider excluding personnel who require IT access with minimal disruption. Develop use cases that fall within the scope of the pilot and identify exceptional use cases that can be addressed based on the success of the initial pilot and lessons learned.

>> * **Identify potential privacy impacts of pilot.** Evaluate the potential privacy impact associated with the planned pilot implementation. This should include an evaluation of the type of data that is being used and/or exchanged to determine if live production data containing any PII will be included. Consider using alternative data sources, if available, or ensure that the live production data is properly protected and disposed of in accordance with the agency‘s privacy and data protection policies.

>> * **Identify metrics for success and determine how evaluation data will be collected.** Collecting evaluation data consists of evaluating the performance of the LACS solution in terms of the number of authentication attempts (successful and unsuccessful), application downtime as a result of solution usage, as well as measuring the acceptance and use of the solution by the pilot participants.

>> * **Identify pilot participants.** Pilot participants are generally identified as part of the application integration and prioritization effort, when specific applications are targeted for involvement in pilot implementations. However, agencies should seek to involve participants who will provide a broad representation of users‘ familiarity with using smart cards, office, position, physical location, and hardware used. Additionally agencies should consider the users‘ willingness to accept the risk associated with use of the new technology and who may be easily helped if they experience problems.

>> * **Formally evaluate the success of the pilot implementation.** When planning for a LACS pilot implementation agencies should plan on holding a formal evaluation of the criteria for success immediately following the program‘s conclusion. This allows the agency to identify and correct any deficiencies with the LACS solution before wide-scale deployment occurs.

<br>

<div style="background-color: #edf1f3;color: black;margin: 10px;padding: 10px">

<h3><span>Privacy Tip</span></h3>
<p><span>While pilot implementations are often small in size and scope, agencies should keep in mind that legal and regulatory requirements for privacy and data protection apply equally to pilot implementations. Agencies should involve appropriate personnel from privacy and security offices to ensure that adequate safeguards are in place prior to implementing pilot activities.</span></p>

</div>

<br>

> When establishing a LACS pilot implementation, agencies should consider several specific factors, which influence not only the success of the pilot but may also impact the agency‘s ability to predict the success of wide-scale deployment. These factors include:

>> * **Define scope of pilot.** Start small with limited number of willing and informed users, using agency PIV cards to access the agency‘s domain. Consider excluding personnel who require IT access with minimal disruption. Develop use cases that fall within the scope of the pilot and identify exceptional use cases that can be addressed based on the success of the initial pilot and lessons learned.

>> * **Identify potential privacy impacts of pilot.** Evaluate the potential privacy impact associated with the planned pilot implementation. This should include an evaluation of the type of data that is being used and/or exchanged to determine if live production data containing any PII will be included. Consider using alternative data sources, if available, or ensure that the live production data is properly protected and disposed of in accordance with the agency‘s privacy and data protection policies.

>> * **Identify metrics for success and determine how evaluation data will be collected.** Collecting evaluation data consists of evaluating the performance of the LACS solution in terms of the number of authentication attempts (successful and unsuccessful), application downtime as a result of solution usage, as well as measuring the acceptance and use of the solution by the pilot participants.

>> * **Identify pilot participants.** Pilot participants are generally identified as part of the application integration and prioritization effort, when specific applications are targeted for involvement in pilot implementations. However, agencies should seek to involve participants who will provide a broad representation of users‘ familiarity with using smart cards, office, position, physical location, and hardware used. Additionally agencies should consider the users‘ willingness to accept the risk associated with use of the new technology and who may be easily helped if they experience problems.

>> * **Formally evaluate the success of the pilot implementation.** When planning for a LACS pilot implementation agencies should plan on holding a formal evaluation of the criteria for success immediately following the program‘s conclusion. This allows the agency to identify and correct any deficiencies with the LACS solution before wide-scale deployment occurs.

<br>

<div style="background-color: #edf1f3;color: black;margin: 10px;padding: 10px">

<h3><span>Lesson Learned</span></h3>
<p><span>The General Services Administration (GSA) recognized that a LACS deployment relies on “quick wins” to demonstrate success and build support throughout the organization for continuing along the LACS maturity curve. “Quick wins” can be achieved through thoughtful application prioritization and pilot integration – select applications with well- defined user groups where user satisfaction and process streamlining can be easily evaluated.</span></p>

</div>























