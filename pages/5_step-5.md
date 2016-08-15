---
layout: page_collection
title: Step 5 - Implement Architecture
permalink: 5_step-5
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

Implementing a LACS solution requires a well-defined solution design backed by measurable requirements that dictate how the solution should function when it is complete. While there are many potential implementation paths that an agency could choose to follow, there are several common areas that can affect the overall success and use of LACS solutions. The checklist blow provides you with a list of common activities that should occur.

## <span style="color: #0C5C89">**Checklist**</span>

> <i class="fa fa-check-square-o"></i> &nbsp;**Authorize the LACS.** Conduct Step 5 of the Risk Management Framework (RMF): Authorize Information System by preparing and submitting the security authorization package to the authorizing official. The authorizing official chooses to accept the risk and authorize the system if the risk associated with operating the LACS is deemed acceptable.

> <i class="fa fa-check-square-o"></i> &nbsp;**Conduct User Acceptance Testing.** Conduct user acceptance testing to ensure that the LACS solution is acceptable to stakeholders and end users and performs appropriately.

<div id="accordion" markdown="1">

### Component Deployment
<div markdown="1">

The first step in deploying LACS is the installation and configuration of the main LACS components. Each LACS solution component has different considerations which must be evaluated as part of the deployment process. The table below contains a list of sample considerations when planning to deploy LACS solution components.

| <center> Solution Component </center> | <center> Deployment Considerations </center> |
|:------------------------------------:|----------------------------------|
| **Identity Manager** | • **Availability of authoritative source(s).** An agency should determine what source(s) are authoritative for digital identity data for its users. Integration with these sources will impact how the Identity Manager is deployed. <br><br> • **Identity data cleansing and normalization.** Identity data within authoritative source(s) must be properly formatted (in accordance with defined standards) and reviewed for consistency and quality prior to integration with the Identity Manager. <br><br> • **Ability to reconcile data changes within authoritative source(s).** An agency should consider how often and how quickly the Identity Manager should detect changes in the authoritative source(s) data. Changes could happen immediately though real-time messaging or in scheduled increments through either flat file reconciliation or Lightweight Directory Access Protocol (LDAP)/database queries. <br><br> • **Define a unique identifier.** An agency should define a unique identifier for its users. The Identity Manager will key off of this identifier to reconcile and synchronize digital identity data with authoritative source(s) and when provisioning to resources. <br><br> •	**Provisioning.** An agency should determine which applications, directories, or Access Managers to provision accounts and digital identity data. Provisioning may lead to increased data integrity as well as improved access control. |
| **Access Manager** | • **Availability of out-of-the-box capabilities.** Many commercially available products offer a number of out-of-the-box service interfaces, web/application server plug-ins, or resource agents that are capable of supporting integration with most standards- based applications. An agency should determine which of these capabilities should be deployed based on its requirements. <br><br> •	**Customization requirements.** An agency should consider the level of effort required to perform modifications and integrate with resources. <br><br> • **Application modification.** Applications will likely require modification to support integration with an Access Manager. Modifications usually include changing the application’s login module to automatically authenticate the account of the userid passed in the Hypertext Transfer Protocol (HTTP) request header. <br><br> • **Performance requirements.** In order to prevent performance issues when externalizing authorization decisions to an Access Manager, it is important to consider how the system will handle multiple queries to the Policy Decision Point (PDP), as well as a PDP’s ability to handle complex queries. |
| **Role Manager** | **Degree of integration.** The Role Manager can be integrated with the Identity Manager and Access Manager. Because the degree of integration dictates the Role Manager’s capabilities to administer roles and handle segregation of duties (SOD), an agency should consider the appropriate level of integration for this. |
| **Directory Server** | • **Performance requirements.** The Directory Server is a LACS’ identity store and sometimes the authentication source. The infrastructure  should  be appropriately scaled to handle the volume of authentication and authorization requests. <br><br> • **Reuse of existing infrastructure.** Most agencies typically have an agency-wide directory. An agency should consider leveraging this existing directory or migrating the directory to one that will serve as the LACS’ identity store. This will prevent duplication of digital identity data and likely reduce the risk of data discrepancies across the identity stores. <br><br> • **Consolidation of directories.** In situations where multiple, fragmented directories exist, agencies should consider consolidating into a single agency directory to streamline the integration process. | 
| **Federated Acccess Manager** | •	**Intra-agency federation.** Organizations (e.g., components/bureaus) within an agency may already have LACS solutions in place. To capitalize on the resources committed and investments made, leveraging a federated access management model to enable user access across the agency should be considered. Regardless of which organization within the agency is the Identity Provider or service provider, a key consideration is the identification and synchronization of digital identity data between the organizations. The agency should strive to enforce a capability that uniquely identifies individuals across the agency in order to more easily federate across existing systems. <br><br> • **Inter-agency federation.** An agency should perform a cost/benefit analysis to determine whether federating across agency boundaries is more cost-effective than requiring each agency to simply provision/manage an account as if the user belonged to that agency. <br><br> **Leveraging standards.** An agency should select a Federated Access Manager that leverages common industry standards for the exchange of identity information, such as Security Assertion Markup Language (SAML) and Kerberos. This will help enable interoperability with other federated access management systems. | 
| **Analytics and Reporting Tool** | • Existing reporting requirements. An agency should examine its existing reporting requirements and model the reporting capabilities of the Analytics and Reporting Tool to meet its needs. <br><br> • **Relevance of log data.** An agency should determine what access event log data is applicable and to whom. The Analytics and Reporting tool should be configured to present this information as well as notifications and alerts. | 

</div>

### Application Integration
<div markdown="1">

Once the primary LACS solution components have been deployed, the next step is integrating the agency‘s applications and resources with the solution. A LACS integration provides enterprise automated provisioning, authentication, authorization, analytics, and reporting and auditing services for the agency‘s resources. An agency should consider the following when integrating applications to deploy these capabilities:

> * **Automated Provisioning.** The Identity Manager uses a number of out-of-the-box plug-ins and services interfaces to connect to agency resources. It works with the Role Manager component to determine which target applications to provision or de-provision based on attributes like employee status, geographic location, or title change. The Identity Manager should perform all tasks of the user life cycle, including transfers, role changes, approval workflow and delegation, and notifications. It should also handle outlier scenarios involving user accounts on the target systems, such as addressing questionable accounts.

<br>

<div style="background-color: #edf1f3;color: black;margin: 10px;padding: 10px">

<h3><span>FAQ</span></h3>
<p><strong>What is the difference between “push” and “pull” provisioning architectures?</strong></p>

<p><span>In “push” provisioning architectures, LACS components initiate the transmission of identity data (attributes, roles, privileges, etc.) through data feeds at predetermined time intervals or based on events, such as when the data is updated. In “pull” provisioning architectures, however, relying parties initiate the transmission of identity data from LACS components by request, when needed. Agencies should examine the viability of both “push” and “pull” architectures based on their unique business needs and technical requirements.</span></p>

</div>
<br>


> * **Authentication.** Authentication responsibility is assigned to the Access Manager. Applications should be integrated with the Access Manager to manage specific user access to web applications across the enterprise. Integration for authentication tools shouldn’t be limited to just web services, but should also have a set of application programming interfaces (APIs) available for tighter integration. The use of digital certificates or shared secrets between the Access Manager and other LACS solution components for authentication services ensures that integrated applications can trust the authentication decisions.

> * **Authorization.** Authorization responsibility belongs to the Access Manager component. The goal is to externalize the Policy Decision Point (PDP). There should also be considerations on how the Policy Enforcement Point (PEP) will capture requests to data. The requests will come either through a Uniform Resource Locator (URL) or a tight integration with the application. Considerations should be made around how tightly coupled (or de-coupled) a PDP and PEP are, and if/how policies for these components are stored, administered, and extracted. Additionally, an agency should consider whether to allow applications to externalize their authorization model and require the Access Manager component to perform fine-grained authorization.

> * **Reporting/Auditing.** Reporting tools should be flexible and able to generate reports based on any number of scenarios. For example, the report tool should handle the generation of reports based on any attributes stored within an identity manager component. It should also be able to generate report activity based on a particular role from the role manager component.

<br>

<div style="background-color: #edf1f3;color: black;margin: 10px;padding: 10px">

<h3><span>FAQ</span></h3>
<p><span>When integrating agency IT resources with an enterprise LACS solution, an agency should analyze existing provisioning (and de-provisioning) workflows and ensure that these workflows are accurately replicated within the automated provisioning capability. This ensures that existing decision points and approval processes are maintained, while achieving the benefits afforded by leveraging technology to streamline paper-based provisioning processes.</span></p>

</div>

</div>
</div>

> <i class="fa fa-check-square-o"></i> &nbsp;**Deploy LACS Solution to Live Production Environment.** Deploy the LACS solution on the agency’s network infrastructure and begin controlling access to protected resources.

<div id="accordion" markdown="1">

### Component Deployment
<div markdown="1">

The first step in deploying LACS is the installation and configuration of the main LACS components. Each LACS solution component has different considerations which must be evaluated as part of the deployment process. The table below contains a list of sample considerations when planning to deploy LACS solution components.

| <center> Solution Component </center> | <center> Deployment Considerations </center> |
|:------------------------------------:|----------------------------------|
| **Identity Manager** | • **Availability of authoritative source(s).** An agency should determine what source(s) are authoritative for digital identity data for its users. Integration with these sources will impact how the Identity Manager is deployed. <br><br> • **Identity data cleansing and normalization.** Identity data within authoritative source(s) must be properly formatted (in accordance with defined standards) and reviewed for consistency and quality prior to integration with the Identity Manager. <br><br> • **Ability to reconcile data changes within authoritative source(s).** An agency should consider how often and how quickly the Identity Manager should detect changes in the authoritative source(s) data. Changes could happen immediately though real-time messaging or in scheduled increments through either flat file reconciliation or Lightweight Directory Access Protocol (LDAP)/database queries. <br><br> • **Define a unique identifier.** An agency should define a unique identifier for its users. The Identity Manager will key off of this identifier to reconcile and synchronize digital identity data with authoritative source(s) and when provisioning to resources. <br><br> •	**Provisioning.** An agency should determine which applications, directories, or Access Managers to provision accounts and digital identity data. Provisioning may lead to increased data integrity as well as improved access control. |
| **Access Manager** | • **Availability of out-of-the-box capabilities.** Many commercially available products offer a number of out-of-the-box service interfaces, web/application server plug-ins, or resource agents that are capable of supporting integration with most standards- based applications. An agency should determine which of these capabilities should be deployed based on its requirements. <br><br> •	**Customization requirements.** An agency should consider the level of effort required to perform modifications and integrate with resources. <br><br> • **Application modification.** Applications will likely require modification to support integration with an Access Manager. Modifications usually include changing the application’s login module to automatically authenticate the account of the userid passed in the Hypertext Transfer Protocol (HTTP) request header. <br><br> • **Performance requirements.** In order to prevent performance issues when externalizing authorization decisions to an Access Manager, it is important to consider how the system will handle multiple queries to the Policy Decision Point (PDP), as well as a PDP’s ability to handle complex queries. |
| **Role Manager** | **Degree of integration.** The Role Manager can be integrated with the Identity Manager and Access Manager. Because the degree of integration dictates the Role Manager’s capabilities to administer roles and handle segregation of duties (SOD), an agency should consider the appropriate level of integration for this. |
| **Directory Server** | • **Performance requirements.** The Directory Server is a LACS’ identity store and sometimes the authentication source. The infrastructure  should  be appropriately scaled to handle the volume of authentication and authorization requests. <br><br> • **Reuse of existing infrastructure.** Most agencies typically have an agency-wide directory. An agency should consider leveraging this existing directory or migrating the directory to one that will serve as the LACS’ identity store. This will prevent duplication of digital identity data and likely reduce the risk of data discrepancies across the identity stores. <br><br> • **Consolidation of directories.** In situations where multiple, fragmented directories exist, agencies should consider consolidating into a single agency directory to streamline the integration process. | 
| **Federated Acccess Manager** | •	**Intra-agency federation.** Organizations (e.g., components/bureaus) within an agency may already have LACS solutions in place. To capitalize on the resources committed and investments made, leveraging a federated access management model to enable user access across the agency should be considered. Regardless of which organization within the agency is the Identity Provider or service provider, a key consideration is the identification and synchronization of digital identity data between the organizations. The agency should strive to enforce a capability that uniquely identifies individuals across the agency in order to more easily federate across existing systems. <br><br> • **Inter-agency federation.** An agency should perform a cost/benefit analysis to determine whether federating across agency boundaries is more cost-effective than requiring each agency to simply provision/manage an account as if the user belonged to that agency. <br><br> **Leveraging standards.** An agency should select a Federated Access Manager that leverages common industry standards for the exchange of identity information, such as Security Assertion Markup Language (SAML) and Kerberos. This will help enable interoperability with other federated access management systems. | 
| **Analytics and Reporting Tool** | • Existing reporting requirements. An agency should examine its existing reporting requirements and model the reporting capabilities of the Analytics and Reporting Tool to meet its needs. <br><br> • **Relevance of log data.** An agency should determine what access event log data is applicable and to whom. The Analytics and Reporting tool should be configured to present this information as well as notifications and alerts. | 

</div>

### Application Integration
<div markdown="1">

Once the primary LACS solution components have been deployed, the next step is integrating the agency‘s applications and resources with the solution. A LACS integration provides enterprise automated provisioning, authentication, authorization, analytics, and reporting and auditing services for the agency‘s resources. An agency should consider the following when integrating applications to deploy these capabilities:

> * **Automated Provisioning.** The Identity Manager uses a number of out-of-the-box plug-ins and services interfaces to connect to agency resources. It works with the Role Manager component to determine which target applications to provision or de-provision based on attributes like employee status, geographic location, or title change. The Identity Manager should perform all tasks of the user life cycle, including transfers, role changes, approval workflow and delegation, and notifications. It should also handle outlier scenarios involving user accounts on the target systems, such as addressing questionable accounts.

<br>

<div style="background-color: #edf1f3;color: black;margin: 10px;padding: 10px">

<h3><span>FAQ</span></h3>
<p><strong>What is the difference between “push” and “pull” provisioning architectures?</strong></p>

<p><span>In “push” provisioning architectures, LACS components initiate the transmission of identity data (attributes, roles, privileges, etc.) through data feeds at predetermined time intervals or based on events, such as when the data is updated. In “pull” provisioning architectures, however, relying parties initiate the transmission of identity data from LACS components by request, when needed. Agencies should examine the viability of both “push” and “pull” architectures based on their unique business needs and technical requirements.</span></p>

</div>
<br>


> * **Authentication.** Authentication responsibility is assigned to the Access Manager. Applications should be integrated with the Access Manager to manage specific user access to web applications across the enterprise. Integration for authentication tools shouldn’t be limited to just web services, but should also have a set of application programming interfaces (APIs) available for tighter integration. The use of digital certificates or shared secrets between the Access Manager and other LACS solution components for authentication services ensures that integrated applications can trust the authentication decisions.

> * **Authorization.** Authorization responsibility belongs to the Access Manager component. The goal is to externalize the Policy Decision Point (PDP). There should also be considerations on how the Policy Enforcement Point (PEP) will capture requests to data. The requests will come either through a Uniform Resource Locator (URL) or a tight integration with the application. Considerations should be made around how tightly coupled (or de-coupled) a PDP and PEP are, and if/how policies for these components are stored, administered, and extracted. Additionally, an agency should consider whether to allow applications to externalize their authorization model and require the Access Manager component to perform fine-grained authorization.

> * **Reporting/Auditing.** Reporting tools should be flexible and able to generate reports based on any number of scenarios. For example, the report tool should handle the generation of reports based on any attributes stored within an identity manager component. It should also be able to generate report activity based on a particular role from the role manager component.

<br>

<div style="background-color: #edf1f3;color: black;margin: 10px;padding: 10px">

<h3><span>FAQ</span></h3>
<p><span>When integrating agency IT resources with an enterprise LACS solution, an agency should analyze existing provisioning (and de-provisioning) workflows and ensure that these workflows are accurately replicated within the automated provisioning capability. This ensures that existing decision points and approval processes are maintained, while achieving the benefits afforded by leveraging technology to streamline paper-based provisioning processes.</span></p>

</div>

</div>
</div>

<br>

> <i class="fa fa-check-square-o"></i> &nbsp;**Conduct User Training.** Develop training materials and conduct user training prior to LACS deployment to ensure that users are capable of accessing their worksites without disruption.

> <i class="fa fa-check-square-o"></i> &nbsp;**Perform Awareness and Outreach.** Conduct awareness and outreach activities in accordance with the Communications Plan developed as part of the Planning Phase. This involves actively communicating to users that a new access control system is being deployed, the benefits and efficiencies that users can expect, and any steps necessary to begin using the new system.





