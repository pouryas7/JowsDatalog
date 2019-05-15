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

# Prerequisites
The user must provide an database connection information, including username, password, db address, db port, and db name. The recomended RDBMS software is [PostgreSQL].  JowsDatalog is a java based tool and needs [JRE].

# Config File

This file has following parameters which must be provided by the user:

  - db_username: The database username (i.e. postgres)
  - db_port: The database port (i.e 5432)
  - db_password: The database password
  - db_address: The database address
  - db_name: The databse name
  - table_prefix: JowsDatalog creates table for each predicate. We can add a prefix to each table.
  - attribute_prefix: JowsDatalog creates table for each predicate. We can add a prefix to each attribute of a table.
  - resumption: Resumption is one part of SCHQAS. The value should be either true/false
  - number_resumption: the number of resumption (an integer)
  - reset_db: Either true/false and indicates that the tool build the database or not. This help us to use the materialized instance after. 
  - repair: future feature, set false.
  - default_weight: future feature, set 1.
  - program_dir: This can be a directory or a file which points to a Datalog+/- program(+).
  - query_dir: This can be a directory or a file which points to the queries defined on top of the program.
  - csv_dir: The directory where CSV files are stored.
  - schema_dir: The direcoty of the schema of CSV files.
  - use_magicSet: Whether the tool should use MagicD+ or not (true/false)
  - use_basicApproach: Whether the tool should use basic approach or not (true/false); preferably false
  - load_CSV: Whether to load CSVs or not (true/false).
  - printQans: Whether to show the answers to queries or not (true/false).

# How to run the binary
Executing JowsDatalog can be done by running following command from command line:
```sh
$ java -jar /PATH_TO_JOWSDATALOG_DIR/JowsDatalog.jar
```
But, before running this command make sure that you have edited the config file. 


[PostgreSQL]: <http://www.postgresqltutorial.com/>
[JRE]: <https://www.oracle.com/technetwork/java/javase/downloads/jre8-downloads-2133155.html>
