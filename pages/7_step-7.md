---
layout: page_collection
title: Configure Systems for Implementation
permalink: 7_step-7
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

When implementing a LACS solution, one of the most important steps is configuring the agency‘s LACS and infrastructure components to work together to support access based on cryptographic authentication of the PIV card. This section discusses configuration changes, including both hardware and software changes, to an agency‘s IT infrastructure (e.g., workstations, networks, and servers) based on the type of LACS solution that is being implemented.

<br>

<div id="accordion" markdown="1">

### Workstation (Desktop/Laptop) Configuration
<div markdown="1">

In order to align with the FICAM architecture and properly use LACS services, agency workstations may require additional components in order to utilize smart cards. These additional components include:

> * **Smart card readers.** Includes internal or external hardware components and associated device drivers necessary to access PKI certificate data stored on the smart card.

> * **Middleware.** A software component that is required to allow communication between the smart card, smart card reader, and workstation.

> * **Third party plug-ins.** A software component that may be required for workstations that run an operating system that does not support certain protocols.

To allow users to authenticate using a PIV card, agency workstations must incorporate smart card readers. Readers may be either internal (built-in) or external (add-on) components, which can be connected to workstations using existing universal serial bus (USB) connections (for external readers). Many systems today provide built-in readers, and operating system software that supports PIV card usage without middleware. Some older versions of operating systems will require middleware to support PIV credential use, and agencies may also want to provide middleware to support advanced card management features. Multiple middleware products, from a variety of approved vendors are available through the GSA FIPS 201 Evaluation Program Approved Products List.

A third party plug-in may be necessary if the workstation OS does not natively support certain protocols. An example would be the inability of an OS to create Online Certificate Status Protocol (OSCP) requests or Server-Based Certificate Validation Protocol (SCVP) requests in support of certificate validation. If the OS does not support OSCP or SCVP, then a third party plug-in can be acquired and implemented to perform these capabilities. 

</div>

### Network Configuration
<div markdown="1">

Performing PIV-based cryptographic logon to an agency‘s network(s) requires the setup and configuration of many different components, all of which must be available and configured properly for PIV card logon to occur successfully. Configuring an agency‘s network to support PIV card logon offers a number of benefits, one such benefit is that the client strongly authenticates to the domain controller. This is accomplished through the establishment of trust and issuance of PKI device certificates to the domain controller. Unless an agency‘s domain controllers are already performing secure communication, it is unlikely they have a PKI device certificate issued to them.

Within the Federal Government, all PKI certificates issued to individuals to assert identity must conform to the Federal PKI Common Policy Framework257  (COMMON).	This is not the case for non-person entities (NPEs), particularly those that are internal facing only.

LACS components are considered high value, and should be segmented from the rest of the network. A compromise of the LACS system provides an attacker with further access to all connected resources. Components should be positioned within network segments based on a least privilege approach. CRLs, OCSP, and SCVP responders are considered public and should be in the demilitarized zone (DMZ), access management agents and proxies should be collocated with the protected agency applications, whether on the enterprise Local Area Network (LAN), or in the DMZ. Primary LACS components, Identity Manager, Access Manager, Role Manager, Directory Server,  Federated Access  Manager,  and  Analytics  & Reporting Tool,  should be configured in a protected subnet with access limited to only essential personnel at a network level. Additionally, networks supporting LACS components must meet NIST standards for fail-over/redundancy capabilities to ensure high availability.

</div>

### Server Configuration
<div markdown="1">

Servers within a LACS infrastructure either host solution components or agency applications. All agency servers should be hardened to federally recommended or required standards, with access limited to only essential personnel. Configuring an agency‘s servers to support PIV card logon requires that the servers be capable of validating PKI authentication certificates presented by users. Each of the various types and models of servers deployed across the Federal Government requires a different level of configuration to support PKI authentication and PIV-based logon as the native capabilities can vary widely based on age, manufacturer, and supporting software. Agencies should work with their server manufacturers and IT personnel to determine what specific configuration steps are necessary to support the LACS implementation effort. Web-based applications utilizing the PIV credential for authentication must perform certificate status validation using CRLs or OSCP requests to ensure the validity of the authentication certificate and possibly SCVP to validate the certificate chain.

</div>
</div>

<br>

## <span style="color: #0C5C89">**Checklist**</span>

> <i class="fa fa-check-square-o"></i> &nbsp;**Ensure workstations are properly configured for LACS.** Workstations should be set up to accept the use of PIV cards. If additional components and/or plug-ins are needed to accept PIV cards, your agency should implement them to ensure employees' workstations are able to authenticate using their PIV cards.

> <i class="fa fa-check-square-o"></i> &nbsp;**Install PKI certificates.** All domain controllers require PKI certificates that have the Enhanced Key Use of Client Authentication and Server Authentication. This is relatively easy to do by installing a Microsoft CA, which comes with predesigned templates for domain controller certificates.

> <i class="fa fa-check-square-o"></i> &nbsp;**Establish mechanism to validate certificate status.** Agencies should determine where Certificate Revocation Lists (CRLs) will be published and how they will be accessible on the network and/or determine how to connect with an OCSP service.

> <i class="fa fa-check-square-o"></i> &nbsp;**Establish trust with the CA.** As part of network configuration, an agency may need to deal with distributing multiple trust chains. This situation occurs when an agency uses PIV card certificates from one provider and receives device certificates from their own Microsoft CA or a different PKI provider.

> <i class="fa fa-check-square-o"></i> &nbsp;**Map Windows user account setting to certificate.** Certificate mapping provides a more secure method for user authentication. With certificate mapping, a specific certificate is linked to the Windows account of a user. A server application can then use public key technology to authenticate the user by means of this certificate.

> <i class="fa fa-check-square-o"></i> &nbsp;**Ensure high network availability.** The network providing access to the CRLs, OCSP services, and path validation services must be highly available. Authentication of PIV cards will fail, if the certificate status or trust chain for the certificate is not available.

> <i class="fa fa-check-square-o"></i> &nbsp;**Ensure your agency's servers can validate PKI authentication certificates.** In order for your agency's servers to support PIV card logon, they should be able to validate PKI authentication certificates. If not, work with your server manufacturers and IT personnel to determine what needs to be done to the servers to support PKI authentication certificates.
















