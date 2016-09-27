---
layout: page_collection
title: Integrate Your Applications
permalink: 9_step-9
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

Once the primary LACS solution components have been deployed, the next step is integrating the agency‘s applications and resources with the solution. A  LACS solution integration provides automated provisioning, authentication, authorization, analytics, and reporting and auditing services for the agency‘s resources. An agency should consider the following when integrating applications to deploy these capabilities:

<br>

## <span style="color: #0C5C89">**Checklist**</span>

> <i class="fa fa-check-square-o"></i> &nbsp;**Ensure the Identity Manager supports automated provisioning.** The Identity Manager should be integrated to perform all tasks of the user life cycle, including transfers, role changes, approval workflow and delegation, and notifications. It should also be integrated to handle outlier scenarios involving user accounts on the target systems, such as addressing orphaned or questionable accounts.

> <i class="fa fa-check-square-o"></i> &nbsp;**Integrate applications with the Access Manager for authentication.** Authentication responsibility is assigned to the Access Manager, so applications should be integrated with the Access Manager to manage specific user access to web applications across the enterprise. Integration for authentication tools shouldn't be limited to just web services, but should also have a set of (APIs) available for tighter integration. The use of digital certificates or shared secrets between the Access Manager and other LACS solution components for authentication services ensures that integrated applications can trust the authentication decisions.

> <i class="fa fa-check-square-o"></i> &nbsp;**Determine authorization model.** Authorization responsibility belongs to the Access Manager component. The goal is to externalize the Policy Decision Point (PDP). There should also be considerations on how the Policy Enforcement Point (PEP) will capture requests to data. The requests will come either through a Uniform Resource Locator (URL) or a tight integration with the application. Considerations should be made around how tightly coupled (or de-coupled) a PDP and PEP are, and if/how policies for these components are stored, administered, and extracted. Additionally, an agency should consider whether to allow applications to externalize their authorization model and require the Access Manager component to perform fine-grained authorization. 

> <i class="fa fa-check-square-o"></i> &nbsp;**Enable a reporting/auditing functionality**. It's important to benchmark reports based on the auditing and reporting requirements of your organization. Reporting tools should be flexible and able to generate reports based on any number of scenarios. For example, the report tool should handle the generation of reports based on any attributes stored within an identity manager component and be able to generate reports based on a particular role from the role manager component.

<br>

<div style="background-color: #edf1f3;color: black;margin: 10px;padding: 10px">

<h3><span>Implementation Tip</span></h3>
<p><span>When integrating agency IT resources with an enterprise LACS solution, you should analyze existing provisioning (and de-provisioning) workflows and ensure that these workflows are accurately replicated within the automated provisioning capability. This ensures that existing decision points and approval processes are maintained, while achieving the benefits afforded by leveraging technology to streamline paper-based provisioning processes.</span></p>

</div>
