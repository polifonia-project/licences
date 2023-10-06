Download the musoW knoweldge graph:

```sparql
fx -q queries/download-musoW.sparql -f TTL -o knowledgegraph/musow.ttl
```

Using the alignments to associate musow resources to dalicc licences

```sparql
fx -q queries/musow-licences.sparql -f TTL -o knowledgegraph/musow-licences.ttl -l knowledgegraph/
```
