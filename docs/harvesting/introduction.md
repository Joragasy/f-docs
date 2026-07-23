# Metadata Harvesting

## Introduction

Metadata harvesting is the process of collecting and aggregating dataset metadata from distributed sources into a centralized catalogue. In the context of CKAN, harvesting enables the automatic retrieval of metadata records using standardised machine-readable formats such as RDF and JSON-LD.

This capability is essential for maintaining an up-to-date and comprehensive data catalogue, particularly when source data is managed across multiple organisations or platforms.

## How It Works

The harvesting framework relies on three key components:

1. **[ckanext-harvest](https://github.com/ckan/ckanext-harvest)** — The core harvesting extension for CKAN. It provides the infrastructure for defining, scheduling, and executing harvest jobs against remote data sources.

2. **[ckanext-dcat](https://github.com/ckan/ckanext-dcat)** — An extension that adds support for the DCAT vocabulary, enabling datasets to be exposed and harvested in RDF and JSON-LD formats.

3. **fedora-harvester** — A custom automation tool developed to streamline the harvesting process. It allows harvest jobs to be configured and executed directly from a CSV definition file, eliminating the need for manual setup through the CKAN interface.
