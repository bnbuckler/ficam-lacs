---
layout: page_collection
title: Step 8 - Deploy Solution Components
permalink: 8_step-8
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

The first step in deploying a modernized LACS is the installation and configuration of the main LACS components. Each LACS solution component has different considerations which must be evaluated as part of the deployment process. The table below contains a list of sample considerations that agencies should assess when planning to deploy LACS solution components.

| <center> Solution Component </center> | <center>Deployment Considerations </center> |
|:-------------------------------------:|-----------------------------------|
| **Identity Manager** | • **Availability of authoritative source(s).** Determine what source(s) are authoritative for digital identity data for its users. Integration with these sources will impact how the Identity Manager is deployed. <br><br> • **Identity data cleansing and normalization.** Identity data within authoritative source(s) must be properly formatted (in accordance with defined standards) and reviewed for consistency and quality prior to integration with the Identity Manager. <br><br> • **Ability to reconcile data changes within authoritative source(s).** Consider how often and how quickly the Identity Manager should detect changes in the authoritative source(s) data. Changes could happen immediately though real-time messaging or in scheduled increments through either flat file reconciliation or Lightweight Directory Access Protocol (LDAP)/database queries. <br><br> • **Define a unique identifier.** Define a unique identifier for its users. The Identity Manager will key off of this identifier to reconcile and synchronize digital identity data with authoritative source(s) and when provisioning to resources. <br><br> • **Provisioning.** Determine which applications, directories, or Access Managers to provision accounts and digital identity data. Provisioning may lead to increased data integrity as well as improved access control. |
| **Access Manager** | • **Availability of out-of-the-box capabilities.** Many commercially available products offer a number of out-of-the-box service interfaces, web/application server plug-ins, or resource agents that are capable of supporting integration with most standards- based applications. Determine which of these capabilities should be deployed based on its requirements. <br><br> • **Customization requirements.** Consider the level of effort required to perform modifications and integrate with resources, even when using out-of-the-box tools, to accept information via headers or assertions when identities are asserted or mapped during run-time authentication. <br><br> • **Application modification.** Applications will likely require modification to support integration with an Access Manager. Modifications usually include changing the application’s login module to automatically authenticate the account of the userid passed in the Hypertext Transfer Protocol (HTTP) request header. <br><br> • **Performance requirements.** In order to prevent performance issues when externalizing authorization decisions to an Access Manager, it is important to consider how the system will handle multiple queries to the Policy Decision Point (PDP), as well as a PDP’s ability to handle complex queries. |
| **Role Manager** | • **Degree of integration.** The Role Manager can be integrated with the Identity Manager and Access Manager. Because the degree of integration dictates the Role Manager’s capabilities to administer roles and handle segregation of duties (SOD), an agency should consider the appropriate level of integration.
| **Directory Server** | • **Performance requirements.** The Directory Server is a LACS’ identity store and sometimes, the authentication source. The infrastructure  should  be appropriately scaled to handle the volume of authentication and authorization requests. <br><br> •	**Reuse of existing infrastructure.** Most agencies typically have an agency-wide directory. An agency should consider using this existing directory or migrating the directory to one that will serve as the LACS’ identity store. This will prevent duplication of digital identity data and likely reduce the risk of data discrepancies across the identity stores. <br><br> • **Consolidation of directories.** In situations where multiple, fragmented directories exist, agencies should consider consolidating into a single agency directory to streamline the integration process and minimize the risk of duplication. |
| **Federated Access Manager** | • **Intra-agency federation.** Organizations (e.g., components/bureaus) within your agency may already have LACS solutions in place. To capitalize on the resources committed and investments made, leveraging a federated access management model to enable user access across the agency enterprise should be considered. Regardless of which organization within the agency is the Identity Provider or service provider, a key consideration is the identification and synchronization of digital identity data between the organizations. You should strive to enforce a capability that uniquely identifies individuals across your agency in order to more easily federate across existing systems. <br><br> • **Inter-agency federation.** Perform a cost/benefit analysis to determine whether federating across agency boundaries is more cost-effective than requiring each agency to simply provision/manage an account as if the user belonged to that agency. Currently, the number of external users who need to access an agency’s applications may not be at a critical mass; however, you should consider potential future business needs and externally-facing services as part of this analysis. <br><br> • **Leveraging standards.** An agency should select a Federated Access Manager that leverages common industry standards for the exchange of identity information, such as Security Assertion Markup Language (SAML) and Kerberos. This will help enable interoperability with other federated access management systems. | 
| **Analytics and Reporting Tool** | •	**Existing reporting requirements.** An agency should examine its existing reporting requirements and model the reporting capabilities of the Analytics and Reporting Tool to meet its needs. <br><br> • **Relevance of log data.** An agency should determine what access event log data is applicable and to whom. The Analytics and Reporting tool should be configured to present this information as well as notifications and alerts. |






















