# #4 Insecure Design

OWASP defines insecure design as "missing or ineffective control design". It is a broad category. 
insecure design vulnerabilty arises when Designer/Developer/QA fails to <b><i> anticipate and evaluate threats <i><b> during design phase       . <br>

## Example of insecure design 

Credential recovery workflow which includes "Question and Answer" is prohibited by NIST. So Using "Question and Answer" as crendential recovery is a insecure design decision.

## Insecure Design mitigation

1. User secure SDLC -consider security right from requirements gathering phase. <br>
2. Test your code - using any robost test suit<br>
3. Implement threat modelling 