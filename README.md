# README
This repository contains ANTLR4 grammar file for Datalog programming language. 
Datalog is a declarative programming language that was introduced as a query language for deductive databases.

Primarily the grammar is based on the following tutorial:
http://blogs.evergreen.edu/sosw/files/2014/04/Green-Vol5-DBS-017.pdf

Note that there are certain changes made to the syntax to introduce typed literals and distinguish between
predicates and variables. Any feedback is most welcome.

## Examples
1. Inserting facts with appropriate types
```
parent("bill", "mary").
parent("mary", "john").
```

2. Horn clauses (or rules)
```
ancestor(?x, ?y) :- parent(?x, ?y).
ancestor(?x, ?y) :- parent(?x, ?z), ancestor(?z, ?y).
```

3. Query that utilizes predicates
```
?- ancestor("bill", ?x).
```
