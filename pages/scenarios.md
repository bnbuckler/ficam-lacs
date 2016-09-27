---
layout: page_collection
title: Common Logical Access Scenarios
permalink: scenarios
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

When implementing a LACS solution for PIV-based access across an enterprise, there are a number of common scenarios that the solution must be capable of supporting. This section identifies and discusses two of these common scenarios, network logon and client authentication to servers. Each subsection explains how these scenarios are accomplished, and introduces specific considerations that agencies should be aware of when configuring and deploying their LACS solution.

<div style="background-color: #edf1f3;color: black;margin: 10px;padding: 10px">

<h3><span>Implementation Tip</span></h3>
<p><span>While transitioning networks and applications to support PIV card logon as part of a LACS effort, consider implementing short term transitional solutions to help mitigate the risk of inadvertently causing users to lose access to IT resources. An example is accepting multiple credentials (e.g., username/password, PIV card, token, etc.) during the transitional period. This ensures that users can continue to logon using the legacy authentication process while preparing for and transitioning to the PIV credential authentication process.</span></p>

</div>

<br>

### <span style="color: #0C5C89">Network Logon</span>

Network logon is the process through which agency users use their PIV cards to access an agency‘s computer networks and shared information systems. Successfully logging onto an agency‘s network using a PIV card is reliant on proper configuration of agency infrastructure and LACS solution components. The process involved in logging onto an agency network involves the user presenting a PIV-based authentication certificate to the network‘s domain controller, validation of the certificate through CRL, OCSP, and  SCVP processes, and  matching of the  user‘s identity to one recognized and accepted by the network‘s identity repository. 

When implementing network logon capabilities agencies should consider the following challenges:

> * **Extracting and matching User Principal Name (UPN).** The UPN must be extracted from the user authentication certificate and matched to an identity stored in the network‘s identity repository (e.g., Microsoft Active Directory, Radiant Logic Virtual Directory Service). This process ensures that the identity repository does not store the certificate information, but possesses the key attribute required for certificate mapping. Alternatively, the certificate could be stored within the identity repository and compared with the live authentication certificate presented. If the UPN can't be extracted from the certificate or matched with an existing identity, then the authentication attempt will fail.

> * **Achieving SSO.** It's possible to achieve SSO through network logon by passing identity assertions in the form of cookies, Kerberos tickets, or encrypted Hypertext Transfer Protocol (HTTP) headers to applications, or through agent-based authentication (i.e., through use of an Access Manager). The application handles the identity assertion and doesn't need to process the user‘s authentication certificate.

<br>

<div style="background-color: #edf1f3;color: black;margin: 10px;padding: 10px">

<h3><span>ROI</span></h3>
<p><span>Enabling remote access servers and virtual private network (VPN) clients to accept the PIV card not only satisfies relevant security requirements related to remote access, but also offers significant benefits over separate tokens or devices. Use of the PIV card eliminates the costs and administrative burden of operating a separate token infrastructure and enables an agency’s users to take advantage of the digital signature and encryption capabilities of the PIV card when working remotely.</span></p>

</div>

<br>

### <span style="color: #0C5C89">Client Authenticatiion to Servers</span>

Client authentication to servers is when users use their PIV cards to access an agency‘s IT resources that reside on web or application servers. Successfully accessing an agency‘s IT resources through a web or application server using a PIV card is reliant on proper configuration of agency infrastructure and LACS solution components. The process through which the authentication occurs is very similar to the process for logging on to an agency‘s network, whereby the user‘s authentication certificate is validated by the server, and the user‘s identity matched to an existing identity within the identity repository.

When implementing a LACS solution, consider enabling two-way Transport Layer Security (TLS) to support client authentication. Also known as mutual TLS authentication, this allows a TLS client to confirm the identity of the TLS server, and vice versa as a means of supporting cross-certificate trust. The TLS client communicates the identity of the user via the authentication certificate to the application or web server.














