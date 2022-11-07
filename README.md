# Polifonia Licences KG

This project includes resources for the Polifonia Licences KG, containing licence information of the resources from third-parties that the project reused.

In what follows, fx refers to the following command line `java -jar sparql-anything-<version>-.jar`.
	
## Download licence descriptions from Dalicc
We reuse a catalogue of machine readable licences from the [Dalicc project](https://www.dalicc.net/).

```
fx -q queries/harvest-dalicc.sparql -f TTL -o knowledgegraph/dalicc.ttl
```

## Knowledge Graph Construction

### Generate `datasets-licences.ttl`
From the spreadhseet in `data/` to the RDF file.

```
fx -q queries/kg.sparql -f TTL -o knowledgegraph/datasets-licences.ttl
```

### Views

```
fx -q queries/terms-view.sparql -l knowledgegraph/
```

### Stats

```
fx -q queries/datasets-by-licence.sparql -l knowledgegraph/

fx -q queries/terms-stats.sparql -l knowledgegraph/
```





