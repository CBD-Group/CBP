
## Abstract

Relation Graph is a graph data deployed on IC that supports SPARQL for data storage and query.

## Motivation

It reduces the data processing threshold of Dapp, improves the development efficiency of Dapp, and allows developers to focus on the realization of business logic.

## Specification
 
**Which users need to use the Relation Graph？**

For Dapp development in Dfinity, developers with data processing needs can use Relation Graph.

**How to use Relation Graph?**

1. Use the provided Relation Graph wasm package and did file( [link](https://github.com/relationlabs/download/raw/main/ic_graph/ic_graphl.zip))，deploy it to mainnet;
2. Authorize accessible users;
3. Dapp accesses Relation Graph canister for data processing;


**What are the specific benefits of using the Relation Graph?**

1. Easy to deploy;
2. Support SPARQL query specification, easy to use;
3. Support conditional query, associated query, sorting, distinct;
4. Custom Schema, convenient for developers to store multiple business module data in a Relation Graph;
5. Support data import and export, convenient for developers to do data maintenance;

**Follow-up plan**

1. Open source, support extension development based on Relation Graph;
2. Dapp scaffolding;
3. Development IDE;
4. Distributed graph database;

## Rationale

Relation Graph is designed to provide data storage and query functions without touching the interests of developers. Developers can deploy it in their own Canister for use.


## Copyright
Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
