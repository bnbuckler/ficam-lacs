---
layout: page_collection
title: Common Design Characteristics
permalink: characteristics
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
In order to successfully build and deploy a LACS solution it is necessary to understand the common characteristics that the solution should include in order to meet the objectives of the FICAM Architecture. These common characteristics can be found in the table below; however it is also important for agencies to consider their specific needs when designing a LACS solution.

<br>

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
















