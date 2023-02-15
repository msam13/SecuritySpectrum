# Threat modelling frameworks

☆ MITRE ATT &CK 
☆ Owasp top 10
☆ STRIDE

Thread modeling is a processing to
understand security threats
determine the risks from those threats
establish appropriate mitigations

Threat modelling process steps :
1. Model (Data flow model)
2. Enumerate threats
3. mitigate
4. validate

## MITRE ATT&CK framework

this framework breaks lifecycle of cyberattack into 14 stages. stages are called “Tactics”
Each Tactic has Techniques and sub techniques 

checking if the system is vulnerable to each of the techiniques and tactics in framework, will give good understanding of potential vulnerablities. 

Along with MITRE ATT & CK framework, there is MITRE CWE (common weakness enumeration). this lists TOP 25 threats.

ATT&CK can better be used for identifying specific threats 

## STRIDE 

STRIDE is Microsoft’s threat modeling framework. 
STRIDE can be used for high - level modelling.

STRIDE (spoofing. Tampering, Repudiation, Information disclosure, Elevation of privledge)
when all are threats are enumerated, each threat is has an associated category (STRIDE)

Microsoft has it’s own threat modeling tools, which takes dataflow diagram as input and produces the list of potential threats to the system. 


## OSWAP top 10
focus is on web application vulnerablities. It has list of exploitable vulnerablities and poor development practices.
This is the best starting point for threat modelling.
Focus is on web application security, but principles can be applied to other softwares as well