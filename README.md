# FreeIPA-Container
Creating a FreeIPA server with OpenShift using podman 
FreeIPA (Identity, Policy, and Audit) is an open-source identity management solution.
FreeIPA is an integrated Identity and Authentication solution for Linux/UNIX networked environments. A FreeIPA server provides centralized authentication, authorization, and account information by storing data about users, groups, hosts, and other objects necessary to manage the security aspects of a network of computers.
 LDAP directory: a common user directory so that all services in both the SDX and workload clusters can consistently resolve users.
 Kerberos KDC: a single common Kerberos realm so that services can authenticate each other, within and between clusters. Kerberos is also used as a user authentication mechanism by some services.
 DNS server: a relatively simple way to discover and reach shared services in an SDX cluster from various workloads.
 Certificate Authority (CA): Some services secure communication channels with TLS, which means they need certificates. A shared CA allows CDP to establish a common trusted root for all connected workloads.

Identity management with FreeIPA

IPA is an identity management framework used to assert who a user is. A subset of users and groups are replicated into IPA (and propagated to the nodes via SSSD). Making the users and groups available on the nodes with consistent user names enables security policies to be migrated from on-prem to the cloud. Users and groups are imported from on-prem and principally managed from the Control Plane UMS (User Management System), with IPA providing the backend propagation.

