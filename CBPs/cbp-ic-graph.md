
## Abstract

IC graph is a graph database based on rust language and supports sparsql query statements. The IC graph can be deployed as an independent canisteror as a dependency for business layer application development. At present, in addition to basic storage and query, IC graph also supports ACL, OGM and other functions.

## Motivation

It reduces the data processing threshold of Dapp, improves the development efficiency of Dapp, and allows developers to focus on the realization of business logic.

## Specification

**Which users need to use the Relation Graph？**

For Dapp development in Dfinity, developers with data processing needs can use Relation Graph.

**How to use Relation Graph?**

1. Use the provided Relation Graph wasm package and did file( [link](https://github.com/relationlabs/download/raw/main/ic_graph/ic_graphl.zip))，deploy it to mainnet;
2. Authorize accessible users;
3. Dapp accesses Relation Graph canister for data processing,use the following APIs:
    ~~~js
        export const idlFactory = ({ IDL }) => {
        return IDL.Service({
            'acl_grant' : IDL.Func([IDL.Text, IDL.Text], [IDL.Text], []),
            'acl_revoke' : IDL.Func([IDL.Text], [IDL.Text], []),
            'acl_show' : IDL.Func([IDL.Nat], [IDL.Text], ['query']),
            'import_schemal' : IDL.Func([IDL.Vec(IDL.Nat8)], [IDL.Text], []),
            'sparql_query' : IDL.Func([IDL.Text, IDL.Text], [IDL.Text], ['query']),
            'sparql_update' : IDL.Func([IDL.Text], [IDL.Text], []),
        });
        };
        export const init = ({ IDL }) => { return []; };
    ~~~


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
