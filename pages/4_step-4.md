---
layout: page_collection
title: Step 4 - Plan for Application Integration
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

LACS solutions achieve their value primarily through integration with an agency‘s IT resources (applications). Once integrated, your agency‘s applications will use the LACS infrastructure to perform PIV-based PKI certificate authentication, and consume additional access control services (i.e., authorization, policy management, audit and reporting, etc.), if provided. Successfully integrating applications requires detailed planning as certain types of applications (e.g., legacy, custom built) are more complex to integrate and require additional time and resources. For this reason, your should gather and assess information about your agency's applications in an effort to categorize and prioritize them for integration.  

<br>

<div style="background-color: #edf1f3;color: black;margin: 10px;padding: 10px">

<h3><span>Implementation Tip</span></h3>
<p><span>When developing your agency’s logical access infrastructure, be sure to factor in support for emerging technologies. With the growing push to take advantage of the benefits offered by cloud-based computing, your LACS should be designed and built in such a way that they are capable of appropriately securing an agency’s applications and services in the cloud.</span></p>

</div>

<br>

Much of the information necessary to perform an application evaluation can be obtained through application information sources available within the organization. However, it may be necessary to gather additional information from application owners and administrators. You may evaluate and prioritize applications manually, which could be beneficial when very similar or few applications exist. However, tools exist to analyze and score applications in a semi-automated fashion, which significantly reduces evaluation time in agencies with many applications.

<br>

<div style="background-color: #edf1f3;color: black;margin: 10px;padding: 10px">

<h3><span>Implementation Tip</span></h3>
<p><span>The Department of Agriculture (USDA) uses Decision Lens to analyze, evaluate, and prioritize their applications for integration with the agency’s LACS infrastructure. This tool evaluates each application’s business continuity, operational risk, multi-agency applicability, and OMB Circular A-123 compliance factors, and automatically ranks them for integration based on a configurable weighting scale.</span></p>

</div>

<br>


## <span style="color: #0C5C89">**Checklist**</span>

> <i class="fa fa-check-square-o"></i> &nbsp;**Evaluate applications' risk profiles.** Risk profiles consist of an evaluation of the application‘s compliance requirements, data sensitivity needs, data privacy requirements, and other artifacts of the FISMA and RMF processes. It's wise to choose low impact applications for inclusion in early integration activities, such as a pilot implementation, to avoid disruptions to sensitive applications during deployment, then prioritize high impact applications once the full enterprise LACS capability has been established.

> <i class="fa fa-check-square-o"></i> &nbsp;**Determine the user base of each application.** In order to achieve widely accepted value across the enterprise, applications should be integrated from a representative set of business and mission areas as soon as possible.

> <i class="fa fa-check-square-o"></i> &nbsp;**Determine the technical readiness of each application.** Applications vary widely in their use of technology, platforms, operating systems, etc., and in maturity and usage. These factors, along with the complexity of the application‘s interfaces and availability of application connectors and service interfaces, contribute to the technical readiness of applications for integration. Agencies should seek to prioritize applications that are the most technically ready as they are generally faster and easier to integrate.

> <i class="fa fa-check-square-o"></i> &nbsp;**Evaluate an application's operational readiness.** Many agencies operate applications that support mission-specific functions, which may dictate certain time periods where operational readiness is of paramount concern. Agencies should seek to integrate applications during the most appropriate timeframe and take into consideration when the resource could tolerate integration efforts.

> <i class="fa fa-check-square-o"></i> &nbsp;**Application Life Cycle Phase.** Prioritize integration of applications that are under development such that they can be linked to the enterprise LACS solution as they are deployed. Applications that are currently operational should be prioritized based on the other factors relevant to the application, such as technical readiness.






















