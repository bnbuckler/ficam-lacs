---
layout: page_collection
title: Step 6 - Operate and Maintain Solution
permalink: 6_step-6/
---
<script>
$(function() {
  $( "#accordion" ).accordion({
    heightStyle: "content",
    collapsible: "true",
    active: "false"
  });
  $( "#accordion2" ).accordion({
    heightStyle: "content",
    collapsible: "true",
    active: "false"
  });
});
</script>

<script src="https://use.fontawesome.com/e20c671b68.js"></script>
-----------------------------------------------------------

One of the key characteristics of developing a LACS solution is providing common logical access management services (entitlement management, authentication, and authorization) at an enterprise level. The solution architecture outlined in the  <a href="http://gsa.github.io/ficam-arch/applications/" target="_blank"> FICAM Architecture ‘Applications View’ </a>, also below, is intended to illustrate the concept of using shared agency resources to provide a common set of logical access services across an agency‘s enterprise. The blue box in the center of the diagram depicts the access management infrastructure with a variety of common components capable of supporting LACS services. These components represent generic products and are not aligned with a particular vendor or solution offering.

<br>

<div style="text-align:center"><img src="{{site.baseurl}}/img/apps-diagram.png"/></div>

<br>

The diagram is intended to serve as a high-level depiction of the preferred design for access management, and is representative of the many solution variations/designs that agencies may choose to implement. This type of solution architecture provides both authentication and authorization services at an enterprise level for all protected resources, and is the recommended means of aligning with the FICAM Architecture. While it is expected that enterprise LACS services will be the primary solution model, this approach may not be appropriate for your agency or for all applications your agency uses. Situations may exist where it is either not feasible to deploy such a solution, or not practical or cost effective to integrate particular applications if such a solution exists. 

<br>

<div id="accordion" markdown="1">

### Enterprise Authentication and Authorization
<div markdown="1">

In the architecture diagram, an agency‘s IT resources are integrated with one or more central LACS solutions that provide both user authentication and authorization services for the integrated resources. This model allows resource owners to use authoritative identity data, centralized authentication, and enterprise access control enforcement to streamline the management of users and privileges for their resource. This approach is recommended for a wide variety of departments and agencies, particularly large independent agencies, agencies that are geographically centralized, or agencies with a large number of standardized web applications. The table below highlights some of the potential benefits and limitations associated with the enterprise authentication and authorization solution.

<br>

| <center> Benefits </center> | <center> Limitations </center> | 
|-----------------------------|--------------------------------|
| •	Agency aligns with the preferred model for alignment with the FICAM Architecture <br><br> • Agency needs can be supported by a number of widely available Commercial Off-The-Shelf (COTS) products/suites <br><br> • Applications gain added security through use of a standardized authentication mechanism <br><br> • Users may be able to experience single sign-on (SSO) capabilities across multiple applications <br><br> • User authorization decisions are based on authoritative entitlement attributes and access privileges <br><br> • Applications receive fine grained authorization decisions based on up-to-date user entitlements <br><br> • Agencies realize an enhanced ability to manage user access across the user life cycle <br><br> • Agencies and resource owners gain an enhanced ability to detect and remediate compliance issues within resources (i.e., segregation of duties [SOD]) and across one or more applications <br><br> • Agencies have the ability to employ role-based access control based on user attributes | • Agencies may require an up-front investment to build, configure, and deploy a LACS solution <br><br> • Agencies may experience difficult and time consuming deployment across the enterprise due to the complexity of the organization <br><br> • Legacy applications may not easily integrate with an enterprise solution <br><br> • Enterprise solutions may not be financially feasible for all agencies, based on size and scope of deployment | 

</div>

### Enterprise Authentication and Decentralized Authorization
<div markdown="1">

Some organizations may require a hybrid approach to providing LACS services where authentication is performed via enterprise authentication services, while authorization decisions are performed natively by the resource. For example, many web access management products, which could make up a part of an agency‘s enterprise authentication services, create and send an identity assertion to each protected application when the user attempts to gain access. The application itself accepts the assertion and relies on locally maintained access privileges to make a user authorization decision. Additional system components within the authentication services address other resource types, such as mainframe applications.

Your agency may choose this type of approach for legacy applications or in situations where it makes sense for a local resource to maintain control over user authorization. For example, certain legacy applications may be incapable of processing more detailed authorization decisions (e.g., role- or attribute-based) or the application does not require robust or detailed authorization capability (e.g., applications with a single user role). 

The table below highlights some of the potential benefits and limitations associated with decentralized authorization approaches.

<br>

| <center> Benefits </center> | <center> Limitations </center> |
|-----------------------------|--------------------------------|
| •	Applications benefit from the added security of a standardized authentication mechanism <br><br> • Users may be able to experience single sign-on (SSO) capabilities across multiple applications <br><br> • Applications maintain local control over authorization decisions <br><br> | • Authorization decisions remain highly dependent on locally managed access privileges <br><br> • Changes to the security model of the application require local code changes <br><br> • Reduced ability to detect and remediate compliance issues within resources (i.e., segregation of duties[SOD]) <br><br> • Authorization may be managed inconsistently across the organization <br><br> • Reduced ability to manage users across the user life cycle <br><br> •	Resource owners must continue to maintain native reporting and auditing capability |

</div>

### Decentralized Authentication and Enterprise Authorization 
<div markdown="1">

You may opt for an additional hybrid solution architecture, which uses a decentralized approach for user authentication while using an enterprise authorization service. In this model, authentication occurs at a local level as applications are configured to accept and validate user PKI certificates. Authorization occurs through an enterprise role and entitlement management service provided by one or more centrally managed authorization products. This type of approach is generally applied in agencies with very diverse or complex applications that require custom connectors or service interfaces to accept authentication decisions, or for high-risk applications that require a direct link between certificate-based authentication and the user‘s session. 

The table below highlights some of the potential benefits and limitations associated with decentralized authorization approaches.

<br>

| <center> Benefits </center> | <center> Limitations </center> |
|-----------------------------|--------------------------------|
| •	Authorization decisions are based on authoritative user entitlement attributes and access privileges <br><br> •	Applications receive fine grained authorization decisions based on up-to-date user entitlements <br><br> • Enhanced ability to manage user access across the user life cycle <br><br> •	Enhanced ability to detect and remediate  compliance issues within resources (i.e., segregation of duties [SOD]) across one or more applications <br><br> •	Ability to employ role-based access control based on user attributes | • Less support for enhanced enterprise level services (i.e., enterprise event auditing, single sign-on [SSO], etc.) <br><br> • Resource owners must continue to maintain native reporting and auditing capability <br><br> •	Reduced ability to provision users in an automated fashion <br><br> • Authentication may be managed inconsistently across the organization <br><br> • Solution viable only at an operating system level; cannot be easily scaled for multiple web applications <br><br> • Highly complex and onerous change management processes | 

</div>

### Decentralized Authentication and Authorization
<div markdown="1">

A decentralized LACS model relies on the native authentication and authorization capabilities within each application to validate users and manage user privileges. When using the PIV credential, this approach is most often achieved by enabling applications to accept and validate PKI certificates to perform user authentication, and then performing authorization against locally maintained access privileges. It is expected that this type of approach will be used in organizations with a small number of applications where implementing a centralized LACS infrastructure is not cost effective. You might also choose this approach if your applications are based on proprietary technology and cannot be easily integrated with enterprise services. Typically a cost/benefit analysis shows that the cost of deploying an enterprise services solution outweighs the benefits that could be achieved. 

The table below lists some of the potential benefits and limitations associated with decentralized LACS approaches.

<br>

| <center> Benefits </center> | <center> Limitations </center> |
|-----------------------------|--------------------------------|
| •	Lower up-front investment required to enable LACS <br><br> • Implementation is generally faster than enterprise solutions <br><br> • Resource owners maintain control over user authentication and authorization decisions <br><br> • Low learning curve for managers and administrators | • Inability to provide enhanced enterprise level services (i.e., enterprise event auditing, single sign- on [SSO], etc.) <br><br> • Resource owners must continue to maintain application specific user account and privilege data <br><br> • Authorization decisions remain highly dependent on locally managed access control lists (ACLs) <br><br> • Reduced ability to provision users in an automated fashion <br><br> • Authentication and authorization may be managed inconsistently across the organization <br><br> • Reduced ability to detect and remediate compliance issues within resources (i.e., segregation of duties [SOD])<br><br> •	No visibility into whether appropriate application access on a per application basis creates policy violations when paired with other application access |

</div>
</div>

<br>

## <span style="color: #0C5C89">**Common Solution Components**

LACS infrastructures consist of a variety of components, including shared agency resources that make up the main Enterprise Logical Access Infrastructure, authoritative identity stores, agency applications, and common components to support PIV card authentication. This section examines the individual solution components that comprise the Enterprise Logical Access Infrastructure. Each of these components can be provided by a variety of Commercial Off-The-Shelf (COTS) software products, in-house agency resources, and custom built tools. In some cases more than one product or solution may be required to achieve the level of functionality described below. This varies based on each agency‘s selected implementation approach, infrastructure, business, and operational requirements. Agencies should examine the primary capabilities of each component discussed in this section when designing LACS solutions in order to ensure that software capabilities are consistent with the ICAM Services Framework, regardless of technology and terminology differences.

<br>

<div style="background-color: #edf1f3;color: black;margin: 10px;padding: 10px">

<h3><span>Privacy Tip</span></h3>
<p><span>When customizing and configuring a Commercial Off-The-Shelf (COTS) solution component or developing a purpose-built tool, consider your agency's existing privacy requirements and regulations. Involving appropriate security and privacy personnel can help ensure that solution components are properly configured and capable of meeting data protection, transmission, storage, and disposal requirements.</span></p>

</div>

<br>

<div id="accordion2" markdown="1">

### Identity Manager
<div markdown="1">

The Identity Manager is designed to correlate identity attributes from a variety of authoritative sources for the purpose of provisioning user accounts to agency resources. When integrating with legacy applications, this may include integrating with the application‘s native user stores (locally maintained user information for administering access control) or providing service interfaces as a means of correlating existing user data with authoritative sources. The Identity Manager automates the provisioning process (i.e., creating, updating, deleting, enabling, and disabling user accounts in applications and/or directories used by enterprise access management solutions).

The Identity Manager manages an array of automated workflows that leverage technology to eliminate manual paper-driven provisioning processes. These workflows include self-service, approval, escalation, manual tracking of approvals, ticketing requests, etc. The Identity Manager eliminates redundant collection of user identity data at the local resource level and prevents violations of segregation of duty (SOD) policies by not allowing accounts and entitlements to be provisioned if they violate a policy. A variety of COTS and purpose-built products are available to serve as the Identity Manager within a LACS infrastructure. 

</div>

### Access  Manager
<div markdown="1">

The Access Manager provides runtime authentication and authorization decisions; enforcement services for protected applications, networks, and operating systems; and can provide an interface for managing access privileges and policies. It complements the Identity Manager by integrating with the directories provisioned by the Identity Manager. Typical products that provide Access Manager functionality offer flexibility and the ability to customize the way that they are integrated into the LACS infrastructure and in the services that are provided at an enterprise level.

The Access Manager performs session management, which enables a single sign-on (SSO) experience from the user perspective, wherein a user only authenticates with the PIV credential once and can access protected applications, provided session and application policy allows it. This eliminates the need for users to authenticate multiple times, thereby streamlining the access process and creating efficiencies for end users. The authentication process occurs between the Access Manager and the individual application in a manner that is transparent to the user.

<br>

<div style="background-color: #edf1f3;color: black;margin: 10px;padding: 10px">

<h3><span>Terminology</span></h3>
<p><strong>Single Sign-On (SSO) –</strong> A mechanism by which a single act of user authentication and log on enables access to multiple independent resources.</p>
<p><span>In practice, many organizations achieve a variation called reduced sign-on, whereby a user experiences SSO for a set of resources but is required to independently authenticate to a small set other resources due to resource-specific security requirements or technical constraints.</span></p>

</div>

<br>

The Access Manager can also serve as a standalone component, without the need to integrate with a dedicated Identity Manager. This is most often the case where an agency chooses to integrate its Access Manager with an existing directory (e.g., Active Directory). This model uses the agency‘s directory as its user store and relies on the Access Manager to manage policies and privileges in addition to making runtime authentication and authorization decisions.

<br>

<div style="background-color: #edf1f3;color: black;margin: 10px;padding: 10px">

<h3><span>Lesson Learned</span></h3>
<p><span>LACS architectures that use a standalone Access Manager (i.e., not integrated with an Identity Manager) may not be a viable solution for agencies that do not have a single authoritative user store, as there is no way to ensure uniqueness of users across the enterprise. A large federal agency attempted to implement a standalone Access Manager solution with disparate data sources and quickly discovered this problem. By implementing an Identity Manager, the agency was able to create unique digital identities and successfully complete their LACS effort.</span></p>

</div>

<br>

A number of COTS and purpose-built products are available as an Access Manager and often include a variety of pre-built or custom resource agents and service interfaces, which are used to integrate with the application and provide enterprise authorization services though policy decision making and enforcement. These agents and services allow the application to intercept unauthenticated and/or unauthorized access attempts to ensure that applications are properly protected.  When designing a LACS solution agencies, consider  the  types of web applications that exist within your IT infrastructure and select an Access Manager that most closely aligns with the your agency's existing investments and infrastructure requirements.

</div>

### Role Manager
<div markdown="1">

The Role Manager integrates with the Identity Manager and supports the process of engineering roles that can be consumed by the Identity Manager and used in the provisioning process. Role engineering can be performed in either a top-down (step-wise definition of roles based on organizational characteristics) or bottom-up (mining existing entitlements from applications) fashion or some combination of the two.

The Role Manager supports SOD policies by preventing the creation of roles that include access entitlements in violation of established policy. The Role Manager allows business owners, resource owners, and resource administrators to revise existing or create new access control rules/policies as business and operational requirements change over time. A variety of COTS and purpose-built products exist to perform Role Manager functions. Many of these products are designed around role-based access control with the emergence of more granular models as many commercial vendors offer tools which provide greater support. When designing a LACS solution, closely examine the Role Manager‘s ability to interact and interface with other LACS components (both existing and new).

</div>

### Directory Server
<div markdown="1">

The Directory Server manages user identity data in a directory format and supports the identity attribute correlation capabilities provided by Identity Manager. This is an optional component within the LACS infrastructure and is typically used when integrating with or consolidating data from one or more directory services, such as Microsoft Active Directory or Radiant Logic Virtual Directory Server.

</div>

### Federated Access Manager
<div markdown="1">

The Federated Access Manager integrates with the Access Manager and Identity Manager to provide access for users that do not have identity records within the LACS (i.e., users from outside of the organization). In cases where an agency operates multiple LACS (e.g., a large agency with multiple independent bureaus/components), the Federated Access Manager may be used to enable access for users from another bureau/component within the agency by obtaining the necessary identity information from the other bureau/component‘s LACS. Within the FICAM Architecture, it is also expected that the Federated Access Manager could support transactions across the Government-to-Government (G2G), Government-to-Business (G2B), and Government-to-Citizen (G2C) domains for users with other credential types. In these cases, the Federated Access Manager obtains the necessary identity information for these users from an appropriate Identity Provider.

In addition to enabling access for users outside of the organization, the Federated Access Manager can also extend the SSO experience for your agency‘s internal users by passing the necessary identity information to external partner applications. This can enhance privacy by providing more granular control over what information is shared and with whom.

</div>

### Analytics and Reporting Tool
<div markdown="1">

The Analytics and Reporting Tool provides the ability to collect and correlate logged data from the other solution components discussed in this section into relevant information. Typically the Analytics and Reporting Tool is used to create a variety of reports that can be presented on a dashboard for various managers and administrators within the organization. The Analytics and Reporting Tool offers the ability to tailor reports and dashboard information based upon the user‘s role and management privileges. For example, a resource administrator may be allowed to view information about his/her resource, but not that of another resource. 

The tool also provides the capability to correlate information across multiple resources. This enables an enhanced ability to identify duplicative or orphaned accounts, detect and resolve segregation of duties (SOD) violations, and periodically re-certify a user‘s access need for certain resources or roles. The Analytics and Reporting Tool supports SOD by identifying where a user has been given access privileges on systems that are in conflict with established SOD policies. Additionally, the tool provides an array of enhanced management capabilities, including the ability to enable continuous monitoring and detect patterns of unauthorized access across multiple resources.

The Analytics and Reporting Tool provides resource owners with access to audit, compliance, and reporting data while reducing the administrative burden inherent with maintaining such a capability natively within the application. The Analytics and Reporting Tool is an optional component within the LACS infrastructure and while its absence does not degrade access control functionality, it should be considered in order to achieve the enhanced capabilities that are offered.

</div>
</div>











