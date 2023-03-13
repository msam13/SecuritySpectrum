# Boolean Satisfiability Problem

we are given a formula (Equation or boolean expression) containing binary variables, that are connected by logical relations (OR and AND). Our aim is to set there variables so that that the formula evaluates to TRUE.

Well know operator: 
- OR 
- AND
- NOT

Other Operators :
- Implication
- equivalence 

### Implication 

An implication is the compound statement of the form "if p then q". It is denoted as p => q, (read as p implies q). It is false, only when P is true and Q is false

-------------- <br>
|p| q  |p=>q| <br>
-------------- <br>
|T| T |T| <br>
|T| F |F| <br>
|F| T |T| <br>
|F| F |F| <br>
--------------<br>

## equivalence 
simply put, equivalence ( p <=> q) is p implies q and q implies p. 

# z3
Using z3 solver, we can input the boolean expression and get the values of variables that makes the expression TRUE.

