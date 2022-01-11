# REBIPP Standards Metadata

**Title:** Brazilian Network on Plant-Pollinator Interactions (REBIPP) Standards Metadata

**Date Version Issued:** 2021-12-03

**Date Created:** 2021-12-03

**Part of Standard:** Not part of any standard

**This version:** `http://rs.rebipp.org.br/index/2021-12-03`

**Latest version:** <http://rs.rebipp.org.br/index>

**Previous version:** [http://rs.rebipp.org.br/index/2021-12-03](README.md)

**Abstract:** This repository contains the source CSV files containing the metadata necessary to generate human- and machine-readable representations of the various components of [Brazilian Network on Plant-Pollinator Interactions (REBIPP)](http://www.rebipp.org.br/) vocabularies in accordance with the [TDWG Standards Documentation Specification](https://github.com/tdwg/vocab/blob/master/sds/documentation-specification.md)). This document represents the human-readable representation of the REBIPP Vocabulary data catalog.

**Contributors:** José Augusto Salim (REBIPP Plant-Pollinator Interaction Vocabulary Maintenance Group)

**Bibliographic citation:** Brazilian Network on Plant-Pollinator Interactions. 2021. Brazilian Network on Plant-Pollinator Interactions (REBIPP) Vocabulary Metadata http://rs.rebipp.org.br/index

# Table of Contents


[1 About directories in this repository](#directories)
[1.1 Relationship of parts of this repository to the metadata model](#directories-relationships)
[1.2 Files contained in current resources directories](#directories-files)
[1.3 Files contained in versions directories](#directories-versions)
[1.4 Retrieving machine readable metadata from the datasets](#directories-machine-readable)
[2 Relationships of directories to resources in the REBIPP Standards model](#directories-resources)
[2.1 Metadata about ratified REBIPP Standards](#standards-metadata)
[2.2 Utility metadata not governed by TDWG Standards](#utility-metadata)


# <a name="directories"></a>1 About directories in this repository

## <a name="directories-relationships"></a>1.1 Relationship of parts of this repository to the metadata model

Each directory in this repository contain metadata for a group of resources at some level in the hierarchy. The data described in each directory can be considered a `dcat:dataset` as described by the [W3C Data Catalog Vocabulary (DCAT)](https://www.w3.org/TR/vocab-dcat/).

Directories whose names do not end in "-versions" contain metadata about current resources.  Directory names ending in "-versions" contain metadata for versions of the current resources described in the corresponding folders that do not end in "-versions".

## <a name="directories-files"></a>1.2 Files contained in current resources directories

Within each current resource directory there is a file whose name corresponds to the containing directory, plus the ".csv" file extension.  That file contains the primary metadata about the resources described in that folder.  For example, in the `terms` directory, the file `terms.csv` is the primary metadata file.  The corresponding file with name ending in "-column-mappings.csv" maps the columns in the primary metadata file to standard metadata properties (similar in function to the meta.xml file of a Darwin Core Archive).  Example: `terms-column-mappings.csv`.

The current resource directory also contains two files that contain link tables that describe one-to-many relationships between the current resource and related resources.  The file with name ending in "-replacements.csv" (example: `terms-replacements.csv`) links current resources to other current resources that replace them.  The file with name ending in "-versions.csv" (example: `terms-versions.csv`) links versions to their corresponding current term.

There are other files in each directory that contain configuration information or other information necessary to generate the machine readable metadata for the resources described in that directory.

## <a name="directories-versions"></a>1.3 Files contained in versions directories

Within each folder describing versions, the primary metadata is in the file whose name corresponds to the containing directory, plus the ".csv" file extension.  For example, in the directory `terms-versions`, the file `terms-versions.csv` is the primary metadata file.  The file with name ending in "-column-mappings.csv" (example: `terms-versions-column-mappings.csv`) maps the columns of the primary version metadata file to standard properties.  The file with name ending in "-replacements.csv" (example: `terms-versions-replacements.csv`) is a link table that links versions to versions that replace them.  Other files in the directory contain configuration or other information needed to generate machine readable metadata for the versions described in the directory.

## <a name="directories-machine-readable"></a>1.4 Retrieving machine readable metadata from the datasets

The IRI `http://rs.rebipp.org.br/index` denotes the REBIPP Data catalog. When dereferenced with an `Accept:` header of `text/html`, this document should be served. When dereferenced requesting `text/turtle`, `application/rdf+xml`, or `application/ld+json`, the data catalog should be served in the RDF/Turtle, RDF/XML, and JSON-LD machine-readable serializations respectively. (The machine-readable data catalogs can be retrieved using the explicit IRIs `http://rs.rebipp.org.br/index.ttl`, `http://rs.rebipp.org.br/index.rdf`, and `http://rs.rebipp.org.br/index.json`.) Note that as of 2020-02-03 the JSON-LD representation does not conform completely to the JSON-LD specification and should not be relied upon as a source of machine-readable metadata. It can, however, be consumed as generic JSON.

The links in the machine-readable metadata can be followed to determine a `dcat:downloadURL` to retrieve a dump of each of the datasets included in the data catalog. The set download URLs can be dereferenced to obtain the complete set of REBIPP standards metadata. The general form of a dataset dumpa is

```
http://rs.rebipp.org.br/dump/datasetname
```
where "datasetname" is the name of the directory containing the dataset.

For more information, see [this blog post](http://baskauf.blogspot.com/2019/04/understanding-tdwg-standards_24.html).

# <a name="directories-resources"></a>2 Relationships of directories to resources in the REBIPP Standards model

## <a name="standards-metadata"></a>2.1 Metadata about ratified REBIPP Standards

 | Level | Current resource IRI pattern | Directory | Version IRI pattern | Directory |
 |---|---|---|---|---|
 | Standard | `http://www.rebipp.org.br/standards/nnn` | [standards](standards) | `http://www.rebipp.org.br/standards/nnn/version/yyyy-mm-dd` | [standards-versions](standards-versions) |
 | Vocabulary | `http://rs.rebipp.org.br/vvv/` | [vocabularies](vocabularies) | `http://rs.rebipp.org.br/version/vvv/yyyy-mm-dd` | [vocabularies-versions](vocabularies-versions) |
 | Term List | `http://rs.rebipp.org.br/vvv/sss/` | [term-lists](term-lists) | `http://rs.rebipp.org.br/vvv/version/sss/yyyy-mm-dd` | [term-lists-versions](term-lists-versions) |
 | Document | `http://rs.rebipp.org.br/sss/doc/docname/` | [docs](docs) | `http://rs.rebipp.org.br/sss/doc/docname/yyyy-mm-dd` | [docs-versions](docs-versions) |
 | Document contributor roles | machine-readable links to contributors | [docs-roles](docs-roles) | N/A | N/A |
 | Literal-value [Plant-Pollinator Vocabulary terms](http://www.rebipp.org.br/standards/ppi) | `http://rs.rebipp.org.br/ppi/terms/ttt` | [terms](terms) | `http://rs.rebipp.org.br/ppi/terms/version/ttt-yyyy-mm-dd` | [terms-versions](terms-versions) |


## <a name="utility-metadata"></a>2.2 Utility metadata not governed by TDWG Standards

 | Level | Current resource IRI pattern | Directory | Version IRI pattern | Directory |
 |---|---|---|---|---|
 | TDWG utility (`dwcutility:`) terms | `http://rs.rebipp.org.br/ppi/terms/attributes/ttt` | [utility](utility) | `http://rs.rebipp.org.br/ppi/terms/attributes/version/ttt-yyyy-mm-dd` | [utility-versions](utility-versions) |
 | Data catalog (DCAT) metadata | `http://rs.rebipp.org.br/dump/datasetname` | [index](index) | N/A | N/A |
 | Executive decisions history | `http://rs.rebipp.org.br/decisions/ttt` | [decisions](decisions)* | N/A** | N/A |
 | Darwin Core translations | multilingual labels (no IRIs) | [dwc-translations](dwc-translations) | N/A | N/A |


 \* The decisions directory also contains [a CSV file](decisions/decisions-links.csv) that links vocabulary terms with the decisions that affected them.

 \** It does not seem necessary at the present time to maintain versions of the decisions themselves, although there are versions of the decisions list.  This could be changed in the future if necessary.
