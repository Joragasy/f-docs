
# How to Harvest

There are two ways to configure harvesting: manually using the graphical interface, or automatically using a script. This guide demonstrates the automatic approach, which is less time-consuming and highly reproducible.

## Prerequisites

Before you begin, verify that you have completed the [Installation](installation.md) steps and connected to the Data Catalogue platform (based on CKAN).

The following image shows the home page of our Data Catalogue:

![CKAN Home Page](../assets/harvesting/ckan-home-page.png)

## Steps

### 1. Get an API Token

Obtain an API token to grant API access and authorize remote calls.

To do so, navigate to **Admin → API Token**, as shown in the following figure.

![Token Generation](../assets/harvesting/token_generation.png)

### 2. Configure fedora-harvester

After installation, verify that the tool is installed and functions correctly.

Run the `fedora-harvester --help` command. You should see the following message:

![fedora harvester before config](../assets/harvesting/fedora-harvester-before-config.png)

This indicates that the tool is functioning correctly, but the configuration has not yet been completed.

Configure fedora-harvester by running the provided command.

Run the `fedora-harvester --help` command again.

You should see all available options:

![fedora harvester after config](../assets/harvesting/fedora-harvester-after-config.png)

### 3. Prepare Your CSV File

All required information for organizations and source creation should be added to the CSV file.

![Example of CSV source list file](../assets/harvesting/example_of_csv_source.png)

In the example above, there are two sources to harvest.

As shown in the `fedora-harvester --help` output, you can either harvest all sources or only a specific row.

To harvest all rows, run the following command:

```bash
  # fedora-harvester -n <number_row> harvest <csv_file_path>
```
