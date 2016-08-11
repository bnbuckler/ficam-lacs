---
layout: page_collection
title: Step 1 - Identify Common Logical Access Scenarios
permalink: /1_step-1/
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
-----------------------------------------------------

When implementing a LACS solution for PIV-based access across an enterprise, there are a number of common scenarios that the solution must be capable of supporting. This section identifies and discusses two of these common scenarios – network logon and client authentication to servers.

## <span style="color: #0C5C89"><a name="plan"></a>**Checklist**</span> 

> <i class="fa fa-check-square-o"></i> &nbsp;**Document LACS Use Cases.** Document detailed LACS use cases, which the designed solution should address in the build phase below. These models should seek to capture existing manual processes that will be automated, along with any exception process workflows that are not part of primary workflow that addresses a large portion of your enterprise’s processes.

<br>

<div style="background-color: #edf1f3;color: black;margin: 10px;padding: 10px">

<h3><span>Implementation Tip</span></h3>
<p><span>While transitioning an agency’s networks and applications to support PIV card logon as part of a LACS effort agencies should consider implementing short term transitional solutions to help mitigate the risk of inadvertently causing users to lose access to IT resources. An example of such a solution is acceptance of multiple credentials (e.g., username/password, PIV card, token, etc.) during the transitional period. This ensures that users can continue to logon using the legacy authentication process while preparing for and transitioning to the target state PIV credential authentication process.</span></p>

</div> 

<br>

> ### Network Logon

> Network logon is the process through which agency users utilize their PIV cards to access an agency‘s computer networks and shared information systems. Successfully logging onto an agency‘s network using a PIV card is reliant on proper configuration of agency infrastructure and LACS solution components. The process involved in logging onto an agency network involves the user presenting a PIV-based authentication certificate to the network‘s domain controller, validation of the certificate through CRL, OCSP, and SCVP processes, and  matching of the  user‘s identity to  one recognized  and accepted by the network‘s identity repository. When implementing network logon capabilities agencies should consider the following challenges:

>> * **Extracting and matching User Principal Name (UPN).** The UPN must be extracted from the user authentication certificate and matched to an identity stored in the network‘s identity repository (e.g., Microsoft Active Directory, Radiant Logic Virtual Directory Service). This process ensures that the identity repository does not store the certificate information, but possesses the key attribute required for certificate mapping. Alternatively, the certificate could be stored within the identity repository and compared with the live authentication certificate presented. If the UPN cannot be extracted from the certificate or matched with an existing identity, then the authentication attempt will fail.

>> * **Achieving SSO.** It is possible to achieve SSO through network logon by passing identity assertions in the form of cookies, Kerberos tickets, or encrypted Hypertext Transfer Protocol (HTTP) headers to applications, or through agent-based authentication (i.e., through use of an Access Manager). The application handles the identity assertion and need not process the user's authentication certificate.

> For configuration and developer guides to support network logon implementation at your agency, please visit the PIV Authentication Playbook site.

<br>

<div style="background-color: #edf1f3;color: black;margin: 10px;padding: 10px">

<h3><span>ROI</span></h3>
<p><span>Enabling remote access servers and virtual private network (VPN) clients to accept the PIV card not only satisfies relevant security requirements related to remote access  but also offers significant benefits over separate tokens or devices. Use of the PIV card eliminates the costs and administrative burden of operating a separate token infrastructure and enables an agency’s users to take advantage of the digital signature and encryption capabilities of the PIV card when working remotely.</span></p>

</div>

<br>

> ### Client Authentication to Servers

> Client authentication to servers is the process through which users utilize their PIV cards to access an agency‘s IT resources that reside on web or application servers. Successfully accessing an agency‘s IT resources through a web or application server using a PIV card is reliant on proper configuration of agency infrastructure and LACS solution components. The process through which the authentication occurs is very similar to the process for logging on to an agency‘s network, whereby the user‘s authentication certificate is validated by the server, and the user‘s identity matched to an existing identity within the identity repository.

> When implementing a LACS solution agencies should consider enabling two-way Transport Layer Security (TLS) to support client authentication. Also known as mutual TLS authentication, this allows a TLS client to confirm the identity of the TLS server, and vice versa as a means of supporting cross-certificate trust. The TLS client communicates the identity of the user via the authentication certificate to the application or web server.





















