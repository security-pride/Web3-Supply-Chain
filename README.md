# Web3-Supply-Chain
Dataset for the paper "Decoding Web3: In-depth Analysis of the Third-Party Package Supply Chain"

# About the Dataset
Due to the data being too large and exceeding the github data size limit, please access it in this [link](https://zenodo.org/records/12593394).



Our supply chain is built on Neo4j graph data. 

We built three different supply chains, i.e. three different Neo4j databases, 
for three different package managers: _NPM_, _PyPI_ and _Cargo_. 

The data are placed in `neo4j-npm.dump`, `neo4j-pypi.dump` and `neo4j-cargo.dump` respectively. 

These are Neo4j 5.20.0 database dump file dumped using `neo4j-admin database dump` command.
```
neo4j-admin database load --from-path=<path-to-dump-file> <database>
```

The nodes in the databases are version-specific packages whose edges represent installation dependencies between packages.

The main attributes of a node are `name`, `version`.
