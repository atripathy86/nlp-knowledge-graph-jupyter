# NLP Knowledge Graph in JupyterLab
This is a Jupyterlab version of https://github.com/neo4j-examples/nlp-knowledge-graph

## Quickstart
- `docker-compose up -d --build`
- Create a file `.env` with customizations of `env-example` in the repo
- This will standup a neo4j community image with the following plugins installed and accessible at http://localhost:7474
    - "apoc" - https://github.com/neo4j/apoc 
    - "n10s" - https://github.com/neo4j-labs/neosemantics
    - "graph-data-science" - https://neo4j.com/docs/graph-data-science/current/installation/
- This will also standup a JupyterLab Data Science image with the following python clients installed at http://localhost:8888/ : 
    - neo4j - https://github.com/neo4j/neo4j-python-driver
    - py2neo - (Alternative to above) https://github.com/py2neo-org/py2neo
    - graphdatascience - https://github.com/neo4j/graph-data-science-client
- Running the Jupyterlab `notebooks/nlp-knowledge-graph.ipynb` will populate the Neo4J DB. Queries will be made in neo4j browser at http://localhost:7474 to visualize ontologies, creation of a knowledge graph from dev.to articles using Wikidata 

## References
- https://github.com/neo4j-examples/nlp-knowledge-graph (source of `:play https://guides.neo4j.com/nlp_knowledge_graphs` )
- Video: https://www.youtube.com/watch?v=17NRCNqqbcA and https://neo4j.com/connections/knowledge-graphs/ 
- https://towardsdatascience.com/how-to-build-a-knowledge-graph-with-neo4j-and-transformers-72b9471d6969

## Building a Knowledge Graph with n10s, APOC
1. neosemantics and APOC NLP to create a software knowledge graph.
    - 