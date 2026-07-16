# Neo4j Enterprise Cluster on Kubernetes

## Architecture

3-node Neo4j causal cluster deployed using Helm.

Components:

- Kubernetes StatefulSets
- Neo4j Enterprise Edition
- Persistent Volumes
- Kubernetes Services
- Helm deployment

## Cluster

Nodes:

core-1
core-2
core-3


## Deployment

helm install core-1 neo4j/neo4j \
 -n neo4j \
 -f helm/core-1-values.yaml


## Validation

kubectl get pods -n neo4j

cypher-shell:
SHOW SERVERS

## Cleanup

helm uninstall core-1 -n neo4j