# ready-to-go-catalogs

## Getting started
#### file structure
    
    ├──  repository name            
    │ ├──   versions             #   version of the chart
    │    ├── flavorname-config.yaml  #default values  for template flavor values
    │    ├── flavorname-readme.md    #specfic readme file per flavor
    │    ├── flavorname-values.yaml  #values per flavor
      ├──    metadata.yaml            #metadata for the template
#### metadata.yaml

```
repositoryName: NAME OF THE REPOSITORY,
repository: URL OF THE REPOSITORY,
chartName: NAME OF THE CHART,
logoImage: URL OF THE CHART,
description: SMALL DESCRIPTION OF THE CHART
tags: RELATED TAGS FOR THE CHART
```
#### flavorname-config.yaml

```
defaultValueArray:
- path: persistentVolume.enable
  value: false
  description: ''
  clusterResources: ''
  regex: []
- path: persistentVolume.storage
  value: 1Gi
  description: ''
  clusterResources: ''
  regex: []
```

| Key | Description | types | required
| ------ | ------ | ------ | ------ |
| path | YAML OR JSON PATH FOR THE VARIABLE | string | required
| value | VALUE FOR THE VARIABLE | string,boolean,array,integer | required
| description | SMALL DESCRIPTION FOR DEFAULT VALUE | text | optional
| clusterResources |  SPECIAL CLUSTER RESOURCES | string | optional
| regex | IF YOU HAVE SPECIAL REGEXS | array | optional
