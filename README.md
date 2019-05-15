# jowsdatalog

Jointly-Weakly-Sticky (JWS) Datalog+/- is an expressive member of Datalog+/-
programs. It is characterized by marking procedure, the existential dependency
graph, and joint acyclicity. Query-answering (QA) can be done in polynomialtime
in data through SChQAS, a chase-based, bottom-up QA algorithm for JWS
Datalog+/- programs. The QA algorithm can be optimized by using a magic-
sets query rewriting technique, MagicD+, for JWS programs. MagicD+ takes
a Datalog+/- program and a query, and rewrites it into a new Datalog+/- program.
The new program can be the input for SChQAS. With the new program,
SChQAS avoids generating irrelevant facts. Designing an Ontology-based data ac-
cess (OBDA) with which QA can be done in polynomial-time in data complexity
for JWS Datalog+/- programs is an open area of research. The main objective of
this thesis is the design and implementation of an OBDA tool, JowsDatalog,
in which SChQAS and MagicD+ are implemented.


