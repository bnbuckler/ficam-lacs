---
layout: page_collection
title: Step 3 - Design Solution
permalink: 3_step-3
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
------------------------------------------------------------------

You will need to document the requirements for the LACS solution and define how the solution should operate within the agency‘s infrastructure. Designing a LACS solution requires your agency to consider the capabilities presented in the FICAM Architecture, existing LACS investments, and your agency‘s overall IT infrastructure. The objective of this effort is to determine how LACS solutions will integrate with the agency‘s IT infrastructure and provide logical access services to the agency‘s applications. Furthermore, you should take steps to ensure that its design does not incorporate any elements that could reduce its ability to authenticate other agencies’ PIV cards.

## <span style="color: #0C5C89">**Checklist**</span>

> <i class="fa fa-check-square-o"></i> &nbsp;**Finalize LACS Solution Requirements.** Conduct a requirements gathering exercise with stakeholders and impacted parties at all organizational levels to document requirements of the LACS solution. These requirements are critical as they will be used to design, build, and configure the LACS capability. View the ‘Common Design Characteristics’ section below for additional guidance.

> <i class="fa fa-check-square-o"></i> &nbsp;**Validate LACS Solution Requirements.** Validate the requirements with the LACS stakeholders to ensure that the LACS solution is properly designed and configured to meet the agency’s needs.

> <i class="fa fa-check-square-o"></i> &nbsp;**Identify and Secure Funding Sources.** Use the LACS business plan to secure funding sources for the effort. All information technology (IT) investments need to include enough funding to support ICAM activities. 

> <i class="fa fa-check-square-o"></i> &nbsp;**Select Security Controls.** Conduct Step 2 of the Risk Management Framework (RMF): <a href="http://csrc.nist.gov/groups/SMA/fisma/controls.html" target="_blank"> Select Security Controls</a> by choosing the appropriate security controls and documenting the selected controls in the security plan.


> <i class="fa fa-check-square-o"></i> &nbsp;**Develop Solution Architecture.** Develop an initial solution architecture for the LACS implementation, which defines the solution components and describes their interactions. View the ‘Common Solution Architecture’ and ‘Common Solution Components’ sections below for additional guidance.


> <i class="fa fa-check-square-o"></i> &nbsp;**Identify Authoritative Stores.** Identify the authoritative store(s) of user information that will be used to enable automated provisioning of user accounts.


> <i class="fa fa-check-square-o"></i> &nbsp;**Establish Common Rules, Roles, and Policies.** Determine the common roles, rules, and policies that shall apply to all applications in the enterprise environment. These common rules serve as a base set of configurable items within a LACS solution, and added granularity can be provided on a per application basis.


> <i class="fa fa-check-square-o"></i> &nbsp;**Map Consolidated Rules, Roles, and Policies to Applications.** Map the base set of rules, roles, and policies to those currently used by the target applications (e.g., the downstream IT resources being protected by the LACS infrastructure).


> <i class="fa fa-check-square-o"></i> &nbsp;**Document System Design.** Draft an initial system design document that clearly states how the system should function within the agency’s environment. The design document and associated requirements are then used during the build phase as a reference for how the LACS system should operate. The design document will also demonstrate how common roles, rules, and policies will be applied to enterprise LACS applications, and will further demonstrate how granular level policies, rules, and roles are supported to meet the LACS application owner needs.


> <i class="fa fa-check-square-o"></i> &nbsp;**Define and Configure Provisioning Workflows.** Define provisioning workflows, which are used to determine how users are granted access to logical resources and what approvals or additional steps are required. This process often involves configuring automated workflows based on existing manual processes. Provisioning workflows are based on a solid understanding of the enterprise approach to common rules, roles, and policies which are applied consistently across managed end-point applications.


> <i class="fa fa-check-square-o"></i> &nbsp;**Develop Demo Application.** Consider development of a demo application that can be used for training business/resource owners on the LACS capabilities that the agency is implementing. Having such a capability provides LACS program management with the ability to showcase all the capabilities and streamline integration processes.


> <i class="fa fa-check-square-o"></i> &nbsp;**Determine Physical Deployed Architecture.** Outline the physical elements that need to reside in data centers, and allow for advanced coordination of the end state solution that will need to be located/hosted there. The agency should include the production environment, pre-production testing environment, user acceptance testing environment, and the development testing environment. These four environments will need to be maintained throughout a solution life cycle to allow for proper testing, regression testing, and solution integration over time.


> <i class="fa fa-check-square-o"></i> &nbsp;**Conduct Detailed Application Assessments.** As part of the application prioritization and integration process, conduct application assessments as a means of gaining information about resource configuration and existing workflows.

> Obtaining the information necessary to complete a comprehensive evaluation of your agency‘s applications as part of the prioritization process can be achieved through a variety of mechanisms. There are a variety of application information sources available within an organization. Much of the information necessary to perform an application evaluation can be obtained by reviewing the information available through these sources. However, it may be necessary to gather additional information from application owners and administrators. Agencies may evaluate and prioritize applications manually, which could be advantageous when very similar or few applications exist. However, tools exist that utilize technology to analyze and score applications in a semi-automated fashion, which significantly reduces evaluation time in agencies with many applications.

<br>

<div style="background-color: #edf1f3;color: black;margin: 10px;padding: 10px">

<h3><span>Implementation Tip</span></h3>
<p><span>The Department of Agriculture (USDA) utilizes Decision Lens to analyze, evaluate, and prioritize their applications for integration with the agency’s LACS infrastructure. This tool evaluates each application’s business continuity, operational risk, multi-agency applicability, and OMB Circular A-123 compliance factors, and automatically ranks them for integration based on a configurable weighting scale.</span></p>

</div>

<br>

> <i class="fa fa-check-square-o"></i> &nbsp;**Conduct Privacy Assessment.** Review the LACS design and solution requirements against established privacy guidelines and agency policies to ensure compliance.

<br>

<div id="accordion" markdown="1">

### Common Design Characteristics
<div markdown="1">

In order to successfully build and deploy a LACS solution it is necessary to understand the common characteristics that the solution should include in order to meet the objectives of the FICAM Architecture. These common characteristics can be found in the table below; however it is also important for agencies to consider their specific needs when designing a LACS solution.

| <center> LACS Characteristic ID </center> | <center> LACS Solution Characteristics </center> | 
|:-----------------------------------------:|---------------------------------------|
| **LACS 1** | Provides a mechanism to support enterprise level provisioning of user identities. |
| **LACS 2** | Provides a workflow engine for executing business logic. |
| **LACS 3** | Provides a set of common enterprise workflows with the flexibility to handle various approval and escalation steps. |
| **LACS 4** | Provides support for identity management industry standards. | 
| **LACS 5** | Provides system interfaces that are flexible and scalable in order to support provisioning requests to existing in scope platforms. |
| **LACS 6** | Provides automated tools for existing account discovery and correlation with individual users to the target applications. |
| **LACS 7** | Provides a framework to determine that the identity profiles created within the Identity Management System (IDMS) have required integrity. |
| **LACS 8** | Supports deployment of connectors and service interfaces to provision identity profiles within an agency-defined timeframe (as defined in Service Level Agreements [SLA]) of receiving the identity/triggering event from sources based on entitlement policies. | 
| **LACS 9** | Provides a management console for defining provisioning rules and policies. |
| **LACS 10**| Provides a provisioning repository for storage of workflow policy rules, in scope application and system attributes, access controls, and logs. |
| **LACS 11** | Provides interfaces to identity repositories that store identities, attributes, entitlements, roles, credentials, and other profile information. |
| **LACS 12** | Provides a secure self-service component for access by users over the intranet. | 
| **LACS 13** | Allows schema extensions to accommodate custom agency data. | 
| **LACS 14** | Provides the ability to define and enforce rules that are specific to an identity and its relationship to the agency. |
| **LACS 15** | Provides bi-directional communications to receive and report changes to local resources. | 
| **LACS 16** | Provides the ability to setup, schedule, monitor and review logs for automated jobs/events. | 
| **LACS 17** | Minimizes the use of customized code, significant schema changes and other application customization. | 
| **LACS 18** | Provides an authentication framework that can be used across the enterprise. | 
| **LACS 19** | Provides easy to use and customer focused authentication methods that utilize the PIV-based PKI certificates for authentication. |
| **LACS 20** | Provides additional identity proofing that can be used to further an authentication attempt, if necessary. |
| **LACS 21** | Provides an interface for native and Commercial Of-The-Shelf (COTS) application to turn over authentication decisions to the LACS components. |
| **LACS 22** | Provides an authorization management framework that includes entitlement administration, enforcement and audit. |
| **LACS 23** | Provides policy administration and authoritative policy store, a policy decision – making system and policy enforcement. This system should be aligned with the authorization management framework. |
| **LACS 24** | Provides policy creation tools that are designed for users and business owners. | 
| **LACS 25** | Provides a role management framework that works in conjunction and integrates with other authorization systems in use. |
| **LACS 26** | Provides an authorization management framework that supports/interoperates with structured data, unstructured data, services and devices. |
| **LACS 27** | Provides an interface for native and COTS application to turn over authorization decisions to the LACS components. | 
| **LACS 28** | Supports authentication and authorization of remote users using the PIV card. |
| **LACS 29** | Provides a requirement for the LACS system that it can differentiate between PKI policy Object Identifiers (OIDs). |
| **LACS 30** | Provides capability to secure IT resources provided by cloud services. |

</div>

### Common Solution Architecture
<div markdown="1">

One of the key characteristics of developing a LACS solution is providing common logical access management services (entitlement management, authentication, and authorization) at an enterprise level. The solution architecture outlined in the FICAM Architecture ‘Applications View’[LINK], also below, is intended to illustrate the concept of using shared agency resources to provide a common set of logical access services across an agency‘s enterprise. The blue box in the center of the diagram depicts the access management infrastructure infrastructure with a variety of common components capable of supporting LACS services. These components represent generic products and are not aligned with a particular vendor or solution offering.

<br>

NEED UPDATED PICTURE

<br>

The diagram is intended to serve as a high-level depiction of the preferred design for access management, and is representative of the many solution variations/designs that agencies may choose to implement. This type of solution architecture provides both authentication and authorization services at an enterprise level for all protected resources, and is the recommended means of aligning with the FICAM Architecture. While it is expected that enterprise LACS services will be the primary solution model, this approach may not be appropriate for your agency or for all applications your agency. Situations may exist where it is either not feasible to deploy such a solution, or not practical or cost effective to integrate particular applications if such a solution exists. 

<br>

### Enterprise Authentication and Authorization


In the architecture diagram, an agency‘s IT resources are integrated with one or more central LACS solutions that provide both user authentication and authorization services for the integrated resources. This model allows resource owners to leverage authoritative identity data, centralized authentication, and enterprise access control enforcement to streamline the management of users and privileges for their resource. This approach is recommended for a wide variety of departments and agencies, particularly large independent agencies, agencies that are geographically centralized, or agencies with a large number of standardized web applications. The table below highlights some of the potential benefits and limitations associated with the enterprise authentication and authorization solution.

| <center> Benefits </center> | <center> Limitations </center> | 
|-----------------------------|--------------------------------|
| •	Agency aligns with the preferred model for alignment with the FICAM architecture <br><br> • Agency needs can be supported by a number of widely available Commercial Off-The-Shelf (COTS) products/suites <br><br> • Applications gain added security through use of a standardized authentication mechanism <br><br> • Users may be able to experience single sign-on (SSO) capabilities across multiple applications <br><br> • User authorization decisions are based on authoritative entitlement attributes and access privileges <br><br> • User authorization decisions are based on authoritative entitlement attributes and access privileges <br><br> • Applications receive fine grained authorization decisions based on up-to-date user entitlements <br><br> • Agencies realize an enhanced ability to manage user access across the user life cycle <br><br> • Agencies and resource owners gain an enhanced ability to detect and remediate compliance issues within resources (i.e., segregation of duties [SOD]) and across one or more applications <br><br> • Agencies have the ability to employ role-based access control based on user attributes | • Agencies may require an up-front investment to build, configure, and deploy a LACS solution <br><br> • Agencies may experience difficult and time consuming deployment across the enterprise due to the complexity of the organization <br><br> • Legacy applications may not easily integrate with an enterprise solution <br><br> • Enterprise solutions may not be financially feasible for all agencies, based on size and scope of deployment | 

<br>

### Enterprise Authentication and Decentralized Authorization


Some organizations may require a hybrid approach to providing LACS services where authentication is performed via enterprise authentication services, while authorization decisions are performed natively by the resource. For example, many web access management products, which could make up a part of an agency‘s enterprise authentication services, create and send an identity assertion to each protected application when the user attempts to gain access. The application itself accepts the assertion and relies on locally maintained access privileges to make a user authorization decision. Additional system components within the authentication services address other resource types, such as mainframe applications.

Your agency may choose this type of approach for legacy applications or in situations where it makes sense for a local resource to maintain control over user authorization. For example, certain legacy applications may be incapable of processing more detailed authorization decisions (e.g., role- or attribute-based) or the application does not require robust or detailed authorization capability (e.g., applications with a single user role). 

The table below highlights some of the potential benefits and limitations associated with decentralized authorization approaches.

| <center> Benefits </center> | <center> Limitations </center> |
|-----------------------------|--------------------------------|
| •	Applications benefit from the added security of a standardized authentication mechanism <br><br> • Users may be able to experience single sign-on (SSO) capabilities across multiple applications <br><br> • Applications maintain local control over authorization decisions <br><br> | • Authorization decisions remain highly dependent on locally managed access privileges <br><br> • Changes to the security model of the application require local code changes <br><br> • Reduced ability to detect and remediate compliance issues within resources (i.e., segregation of duties[SOD]) <br><br> • Authorization may be managed inconsistently across the organization <br><br> • Reduced ability to manage users across the user life cycle <br><br> •	Resource owners must continue to maintain native reporting and auditing capability |

<br>

### Decentralized Authentication and Enterprise Authorization 


Your agency may opt for an additional hybrid solution architecture, which uses a decentralized approach for user authentication while using an enterprise authorization service. In this model, authentication occurs at a local level as applications are configured to accept and validate user PKI certificates. Authorization occurs through an enterprise role and entitlement management service provided by one or more centrally managed authorization products. This type of approach is generally applied in agencies with very diverse or complex applications that require custom connectors or service interfaces to accept authentication decisions, or for high-risk applications that require a direct link between certificate-based authentication and the user‘s session. 

The table below highlights some of the potential benefits and limitations associated with decentralized authorization approaches.

| <center> Benefits </center> | <center> Limitations </center> |
|-----------------------------|--------------------------------|
| •	Authorization decisions are based on authoritative user entitlement attributes and access privileges <br><br> •	Applications receive fine grained authorization decisions based on up-to-date user entitlements <br><br> • Enhanced ability to manage user access across the user life cycle <br><br> •	Enhanced ability to detect and remediate  compliance issues within resources (i.e., segregation of duties [SOD]) across one or more applications <br><br> •	Ability to employ role-based access control based on user attributes | • Less support for enhanced enterprise level services (i.e., enterprise event auditing, single sign-on [SSO], etc.) <br><br> • Resource owners must continue to maintain native reporting and auditing capability <br><br> •	Reduced ability to provision users in an automated fashion <br><br> • Authentication may be managed inconsistently across the organization <br><br> • Solution viable only at an operating system level; cannot be easily scaled for multiple web applications <br><br> • Highly complex and onerous change management processes | 

<br>

### Decentralized Authentication and Authorization


A decentralized LACS model relies on the native authentication and authorization capabilities within each application to validate users and manage user privileges. When using the PIV credential, this approach is most often achieved by enabling applications to accept and validate PKI certificates to perform user authentication, and then performing authorization against locally maintained access privileges. It is expected that this type of approach will be used in organizations with a small number of applications where implementing a centralized LACS infrastructure is not cost effective. An agency might also choose this approach if its applications are based on proprietary technology and cannot be easily integrated with enterprise services. Typically these organizations perform a cost/benefit analysis, and discover that the cost of deploying an enterprise services solution outweighs the benefits that could be achieved. 

The table below lists some of the potential benefits and limitations associated with decentralized LACS approaches.

| <center> Benefits </center> | <center> Limitations </center> |
|-----------------------------|--------------------------------|
| •	Lower up-front investment required to enable LACS <br><br> • Implementation is generally faster than enterprise solutions <br><br> • Resource owners maintain control over user authentication and authorization decisions <br><br> • Low learning curve for managers and administrators | • Inability to provide enhanced enterprise level services (i.e., enterprise event auditing, single sign- on [SSO], etc.) <br><br> • Resource owners must continue to maintain application specific user account and privilege data <br><br> • Authorization decisions remain highly dependent on locally managed access control lists (ACLs) <br><br> • Reduced ability to provision users in an automated fashion <br><br> • Authentication and authorization may be managed inconsistently across the organization <br><br> • Reduced ability to detect and remediate compliance issues within resources (i.e., segregation of duties [SOD])<br><br> •	No visibility into whether appropriate application access on a per application basis creates policy violations when paired with other application access |

</div>

### Common Solution Components
<div markdown="1">

LACS infrastructures consist of a variety of components, including shared agency resources that make up the main Enterprise Logical Access Infrastructure, authoritative identity stores, agency applications, and common components to support PIV card authentication. This section examines the individual solution components that comprise the Enterprise Logical Access Infrastructure. Each of these components can be provided by a variety of Commercial Off-The-Shelf (COTS) software products, in-house agency resources, and custom built tools. In some cases more than one product or solution may be required to achieve the level of functionality described below. This varies based on each agency‘s selected implementation approach, infrastructure, business, and operational requirements. Agencies should examine the primary capabilities of each component discussed in this section when designing LACS solutions in order to ensure that software capabilities are consistent with the ICAM Services Framework, regardless of technology and terminology differences.

<br>

### Identity Manager

The Identity Manager is primarily designed to correlate identity attributes from a variety of authoritative sources for the purpose of provisioning user accounts to agency resources. When integrating with legacy applications, this may include integrating with the application‘s native user stores (locally maintained user information for administering access control) or providing service interfaces as a means of correlating existing user data with authoritative sources. The Identity Manager automates the provisioning process (i.e., creating, updating, deleting, enabling, and disabling user accounts in applications and/or directories used by enterprise access management solutions).

The Identity Manager manages an array of automated workflows that use technology to eliminate manual paper-driven processes. These workflows include self-service, approval, escalation, manual tracking of approvals, ticketing requests, etc. The Identity Manager eliminates redundant collection of user identity data at the local resource level and prevents violations of segregation of duty (SOD) policies by not allowing accounts and entitlements to be provisioned if they violate a policy. A variety of COTS and purpose-built products are available to serve as the Identity Manager within a LACS infrastructure.

<br>

### Access Manager 

The Access Manager provides runtime authentication and authorization decisions; enforcement services for protected applications, networks, and operating systems; and can provide an interface for managing access privileges and policies. Within the desired LACS solution architecture the Access Manager complements the Identity Manager by integrating with the directories provisioned by the Identity Manager. Typical products that provide Access Manager functionality offer flexibility and the ability to customize the way that they are integrated into the LACS infrastructure and in the services that are provided at an enterprise level.

The Access Manager performs session management, which enables a single sign-on (SSO) experience from the user perspective, where a user only authenticates with the PIV credential once and can access protected applications. This eliminates the need for users to authenticate multiple times, creating a more streamlined and efficient process for users. 

<br>

<div style="background-color: #edf1f3;color: black;margin: 10px;padding: 10px">

<h3><span>Terminology</span></h3>
<p><span><strong>Single Sign-On (SSO) – </strong> A mechanism by which a single act of user authentication and log on enables access to multiple independent resources.
In practice, many organizations achieve a variation called reduced sign-on, whereby a user experiences SSO for a set of resources but is required to independently authenticate to a small set other resources due to resource-specific security requirements or technical constraints.</span></p>

</div>

The Access Manager can also serve as a standalone component, without the need to integrate with a dedicated Identity Manager. This is most often the case where an agency chooses to integrate its Access Manager with an existing directory (e.g., Active Directory). This model uses the agency‘s directory as its user store and relies on the Access Manager to manage policies and privileges in addition to making runtime authentication and authorization decisions. While this is a valid approach, the guidance presented in this section aligns with the preferred solution architecture and assumes that the Access Manager is integrated with an Identity Manager component, unless otherwise indicated.

<br>

<div style="background-color: #edf1f3;color: black;margin: 10px;padding: 10px">

<h3><span>Lesson Learned</span></h3>
<p><span>LACS architectures that use a standalone Access Manager (i.e., not integrated with an Identity Manager) may not be a viable solution for agencies that do not have a single authoritative user store, as there is no way to ensure uniqueness of users across the enterprise. A large federal agency attempted to implement a standalone Access Manager solution with disparate data sources and quickly discovered this problem. By implementing an Identity Manager, the agency was able to create unique digital identities and successfully complete their LACS effort.</span></p>

</div>

<br>

A number of COTS and purpose-built products are available as an Access Manager. They often include a variety of pre-built or custom resource agents and service interfaces, which are used to integrate with the application and provide enterprise authorization services through policy decision making and enforcement. These agents and services allow the application to intercept unauthenticated and/or unauthorized access attempts to ensure that applications are properly protected.  When designing a LACS solution agencies should consider the types of web applications that exist within their IT infrastructure and select an Access Manager that most closely aligns with the agency‘s existing investments and infrastructure requirements.

<br>

### Role Manager

The Role Manager integrates with the Identity Manager and supports the process of engineering roles that can be consumed by the Identity Manager and used in the provisioning process. Role engineering can be performed in either a top-down (step-wise definition of roles based on organizational characteristics) or bottom-up (mining existing entitlements from applications) fashion or some combination of the two. 

The Role Manager supports SOD policies by preventing the creation of roles that include access entitlements in violation of established policy. The Role Manager allows business owners, resource owners, and resource administrators to revise existing or create new access control rules/policies as business and operational requirements change over time. A variety of COTS and purpose-built products exist to perform Role Manager functions. Many of these products are designed around role-based access control with the emergence of more granular models as many commercial vendors offer tools which provide greater support. When designing a LACS solution agencies should closely examine the Role Manager‘s ability to interact and interface with other LACS components (both existing and new).

<br>

### Directory Server 

The Directory Server manages user identity data in a directory format and supports the identity attribute correlation capabilities provided by Identity Manager. This is an optional component within the LACS infrastructure and is typically used when integrating with or consolidating data from one or more directory services, such as Microsoft Active Directory or Radiant Logic Virtual Directory Server.

<br>

### Federated Access Manager 

The Federated Access Manager integrates with the Access Manager and Identity Manager to provide access for users that do not have identity records within the LACS (i.e., users from outside of the organization). In cases where an agency operates multiple LACS (e.g., a large agency with multiple independent bureaus/components), the Federated Access Manager may be used to grant access to users from another department within the agency by obtaining the necessary identity information from that department’s LACS. Within the FICAM architecture, it is also expected that the Federated Access Manager could support transactions across the Government-to-Government (G2G), Government-to-Business (G2B), and Government-to-Citizen (G2C) domains for users with other credential types. In these cases, the Federated Access Manager obtains the necessary identity information for these users from an appropriate Identity Provider.

The Federated Access Manager can also extend the SSO experience for an agency‘s internal users by passing the necessary identity information to external partner applications. This can enhance privacy by providing more control over what information is shared and with whom.

<br>

### Analytics and Reporting Tool 

The Analytics and Reporting Tool provides the ability to collect and correlate logged data from the other solution components discussed in this section into relevant information. Typically the Analytics and Reporting Tool is used to create a variety of reports that can be presented on a dashboard for various managers and administrators within the organization. The Analytics and Reporting Tool offers the ability to tailor reports and dashboard information based upon the user‘s role and management privileges. For example, a resource administrator may be allowed to view information about his/her resource, but not that of another resource. 

The tool also provides the capability to correlate information across multiple resources. This results in an enhanced ability to identify duplicative or orphaned accounts, detect and resolve segregation of duties (SOD) violations, and periodically re-certify a user‘s access need for certain resources or roles. The Analytics and Reporting Tool supports SOD by identifying where a user has been given access privileges on systems that are in conflict with established SOD policies. The tool also provides an array of enhanced management capabilities, including the ability to enable continuous monitoring and detect patterns of unauthorized access across multiple resources.

The Analytics and Reporting Tool provides resource owners with access to audit, compliance, and reporting data while reducing the administrative burden inherent with maintaining such a capability natively within the application. The Analytics and Reporting Tool is an optional component within the LACS infrastructure and while its absence does not degrade access control functionality, agencies should consider implementing it in order to achieve the enhanced capabilities that are offered.

</div>
</div>

















