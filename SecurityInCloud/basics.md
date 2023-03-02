# Securing DevOps AKA Continuous security

DevOps is the process of continuously improving software products through rapid release cycles, global automationi of integration and delivery piplines, and close collaboration between teams. Rapid release cycles leaves little room for thorough security reviews

At the core of DevOps is Continuos integration CI, Continuos delivery CD and Infrastructure as a serive IaaS. Reduced management is a result of using DevOps. 


## Infrastructure as a service

Infrastructure as a service is the cloud. Data centre, network, server are entirely operated by a third party. IaaS doesn't necessarily mean outsourcing to a third party, organisations can deploy and operate IaaS in-house using Kubernetes or Openstack.


## Security in Devops

In DevOps, everyone in product pipeline is focused on CUSTOMER
Product manager - engagement and retention ratios
Developers - ergonomics and usabilty
Operators - uptime and response times

In contrast, security teams focus on security centric goals like,
Compliance with security standard
Number of security incidents
count of unpatched vulnerabilities on production systems

This disconnect in goal hurts communication and efficiency. For example, To meet goals, developer and operators ignore security recommendations. 
security team blocks projects making use of unsafe techinques and recommends unrealistic solutions


both the sides hold valid arguements, and are well intended, but fail to understand and adapt to motivation of the other

In DevOps we bring together development and operation, likewise when security becomes integral part of DevOps, security engineers can build controls directly into the product

## Continuous security

Continuous security is composed of three areas 
1. Test driven security TDS
2. Monitoring and responding to attack
3. Assessing risks and maturing security

### Test driven security
First step of a security program is to define, implement, and test security controls. security testing should be handled in the CI and CD pipelines automatically all the time. 

Easy traget for attackers are web framework with security vulnerabilties, admin page open to internet with guessable password, security credentials leaked in opensource, out of date systems etc. So FIRST GOAL in implementing continuous security strategy is to take care of baseline: apply elementart set of controls on the application and infrastructure of the organization and test them continuously. like,
- SSH root login must be disabled on all systems
- system and applications must be patched to latest version within 30days of its release
- web application must use HTTPS, never HTTP
- Admin interface must be behind VPN

#### Application security
protection against CSS, SQL injection, brute force etc.

#### Infrastructure security
VPNs, SSH gateways

#### Pipeline security
compromising CI/CD pipeline can grant an attacker full control over the software that runs in production, mechanisms like commit or container signing should be implemented

### Monitoring and responding to attacks
Online services will get broken eventually, when such incidents happen security must be prepared to react. second phase of continuous security is to monitor and respond to threats and protect the serviced and data the organization relies on.
- ####  Logging and fraud detection 
- #### Detecting intrusions
- #### Responding to incidents

### Assessing risk and maturing security
Risk management and security testing will help organizations refocus thier security efforts and invest thier resources more efficiently.