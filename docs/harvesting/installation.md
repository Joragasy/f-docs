
# Installation

Before setting up harvesting, you need to install three key components:

1. **ckanext-harvest** – the core harvesting framework for CKAN
2. **ckanext-dcat** – extension for handling DCAT datasets and vocabularies
3. **A fedora-harvesting automation tool** – developed to streamline and automate the harvesting process from csv file.

This guide assumes you already have a running CKAN instance.

## Prerequisites

- A working CKAN installation (version 2.9 or later recommended)
- Python 3.7+
- pip and virtualenv (if using virtual environments)
- Git

## Installing ckanext-harvest

Provides the core harvesting framework for fetching metadata from remote sources using protocols like OAI-PMH, CSW, and SPARQL.

```bash
# Navigate to your CKAN virtual environment
cd /usr/lib/ckan/default
source bin/activate

# Install from PyPI
pip install -e git+https://github.com/ckan/ckanext-harvest.git#egg=ckanext-harvest

# Alternatively, install the latest release
pip install ckanext-harvest
```

Add `harvest` to the `ckan.plugins` line in your `ckan.ini` configuration file:

```ini
ckan.plugins = ... harvest
```

## Installing ckanext-dcat

Adds support for DCAT vocabulary to expose and harvest datasets in RDF and JSON-LD formats.

```bash
# In the same virtual environment
pip install -e git+https://github.com/ckan/ckanext-dcat.git#egg=ckanext-dcat

# Or install via PyPI
pip install ckanext-dcat
```

Add `dcat` to the `ckan.plugins` line in `ckan.ini`:

```ini
ckan.plugins = ... harvest dcat
```

## Installing the Fedora-Harvester Automation Tool
This tool helps us to automate CKAN harvest jobs from a CSV definition file via the ckanext-harvest API.

Run the following command :
```bash
# Clone the custom tool repository
git clone https://gitlab.akka.eu/fedora/fedora-harvester.git
cd ckan-harvest-automation

# Install dependencies
pip install -r requirements.txt

# Install the extension
pip install .

```

## Final Configuration

After installing all three extensions, restart CKAN:

```bash
# If using supervisor
sudo supervisorctl restart ckan
```

Verify the installation:

```bash
ckan -c /etc/ckan/default/ckan.ini sysadmin add admin
ckan -c /etc/ckan/default/ckan.ini harvester init
```

## Troubleshooting

- Ensure all extensions are in the `ckan.plugins` line in the correct order.
- Check the CKAN error log for missing dependencies.
- Verify the database tables were created by the harvest init command.

For more details, refer to the official documentation:
- [ckanext-harvest](https://github.com/ckan/ckanext-harvest)
- [ckanext-dcat](https://github.com/ckan/ckanext-dcat)
