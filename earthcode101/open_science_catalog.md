# Open Science Catalog
[http://opensciencedata.esa.int/](http://opensciencedata.esa.int/)

![OSC-main](https://github.com/EOEPCA/open-science-catalog-metadata/assets/120453810/9f3ae080-47fd-494b-bceb-ba9db48f0799)

Data discovery and access in EarthCODE are facilitated through the Open Science Catalog, which provides a structured way to explore and retrieve scientific datasets, metadata, and dependencies. This ensures that researchers can efficiently find and integrate the right data into their projects while promoting transparency and reproducibility.

This section will guide you through the key aspects of data discovery and access, including how to search for datasets, retrieve data via APIs, upload and manage your own data, and incorporate it into workflows for scientific research.

What you'll find in this section:

- [Open Science Catalog](#open-science-catalog)
  - [Introduction to the Open Science Catalog](#introduction-to-the-open-science-catalog)
    - [Accessing the Open Science Catalog](#accessing-the-open-science-catalog)
    - [The Open Science Catalog Landing Page](#the-open-science-catalog-landing-page)
    - [Key Features of the Open Science Catalog](#key-features-of-the-open-science-catalog)
  - [Discovering Catalog Content](#discovering-catalog-content)
    - [Search](#search)
  - [Start Discussions Directly From the Catalog](#start-discussions-directly-from-the-catalog)
  - [Standardized Metadata and Taxonomies for FAIR Data Access](#standardized-metadata-and-taxonomies-for-fair-data-access)
  - [Metrics and Statistics About the EarthCODE Catalog](#metrics-and-statistics-about-the-earthcode-catalog)
    - [Metrics](#metrics)
    - [Statistics](#statistics)


## Introduction to the Open Science Catalog

The Open Science Catalog (OSC), a key component of the ESA EO Open Science framework, is a publicly available web-based application designed to provide easy access to scientific datasets, geoscience products, and scientific resources developed under ESA-funded Earth Observation (EO) research projects. These resources vary in geographical and temporal extent, production methodology, validation, and quality, supporting a wide range of scientific applications. The OSC supports data discovery, access, and integration, promoting Open Science principles.

### Accessing the Open Science Catalog

You can explore the Open Science Catalog from any web browser by navigating to:

👉 [https://opensciencedata.esa.int/](https://opensciencedata.esa.int/)

Upon entering the portal, you will see a welcome page that introduces the catalog and its functionalities. The catalog organizes resources into six thematic research domains, allowing users to easily browse and discover relevant projects, products, workflows, and experiments.

From the landing page, you can also access:

- Search tools for locating products
- Catalog to browse available products
- Metrics to explore data availability statistics
- API capabilities for programmatic access

![OSC-main-page](https://github.com/EOEPCA/open-science-catalog-metadata/assets/120453810/a97e40c1-0f69-4204-9aef-95030c5a8455)

### The Open Science Catalog Landing Page

The OSC front-end serves as the primary user interface, enabling scientists and other users to interact with the system and access its contents. Through this interface, users can search for scientific products, workflows, and experiments. Logged in users can also contribute to the catalog by submitting new entries or requesting updates to existing content.

Exploration begins from the landing page where user can select one of six themes that group products by the specific research domain:

![themes](https://github.com/EOEPCA/open-science-catalog-metadata/assets/120453810/070f3e88-f2a4-4956-bfc7-00e2a660cbb2)

Each theme lists the number of objects associated to that theme via the `osc:themes` field in the STAC Catalog or STAC Collection. This makes entries discoverable by specific domain names.

![cryosphere-theme](https://github.com/EOEPCA/open-science-catalog-metadata/assets/120453810/b1e33838-484d-45c2-bdc0-52c5785c7eef)

From this page users can proceed with Product's further exploration display and review the full description and metadata of a given product and access data.
![product-page-1](https://github.com/EOEPCA/open-science-catalog-metadata/assets/120453810/2c89b757-2da8-41ef-9422-0456d583c97c)

### Key Features of the Open Science Catalog

The majority of the entries only hold metadata for each Product and Project. The actual data and its documentation are maintained and accessible by the data providers, outside of esa.int. This catalog provides the metadata and links to the data as it exists in those many other locations.

The Open Science Catalog is free to use by any user with access to the Internet. Contributing to the catalog (ingesting new products or updating existing) is reserved to authorized users only (project PIs, data owners).

The Open Science Catalog is not only a projects' metadata browser. It brings new functionalities and makes them available to scientific community of users, such as:

- Discovery and access for geospatial products + documentation (or/and code)
- Unified metadata across heterogeneous sources
- Common dictionary
- Open to community curation & contribution
- Synoptic view for EO gap analysis


## Discovering Catalog Content

The OSC Catalog page is built upon the open-source STAC Browser application, allowing users to explore the available contents stored in a static STAC Catalog. This catalog consists of inter-linked JSON files along with supplementary metadata. The catalog facilitates the discovery of the following elements:

- Themes
- Variables
- EO-Missions
- Projects
- Products
- Workflows
- Experiments

Each entry lists the number of objects of the selected type, which are represented as a STAC Catalog, STAC Collection, or OGC API Record. These objects use the OSC STAC extension to reference elements of other groups they are associated with, e.g., a Product has an `osc:variables` field, that lists the measurement variables this product is comprised of. More information on how the items are linked is provided in the [Uploading Your Data](Contributing%20to%20the%20EarthCODE%20Catalog) section.

![STACBrowser-OSC](https://github.com/EOEPCA/open-science-catalog-metadata/assets/120453810/257daa0c-a567-4ed2-a8bc-3fb594079b2c)

The **Overview** button on the top of the page provides the option to navigate between folders in the current Open Science Catalog structure.

STAC Browser allows to filter entries by their title, order them by name, and display them either as tiles or as list. As a minimum requirement for each STAC Catalog, the date of the latest update is provided in a metadata field.

![EO-missions-page](https://github.com/EOEPCA/open-science-catalog-metadata/assets/120453810/4b49bdee-61e3-4481-96a3-6416be261761)

Each element in the catalog has an associated description, link, and product(s) related to that element. In this example we can see 51 Products associated with the Aqua (EOS/PM-1) EO-Mission.

![Aqua-eomission](https://github.com/EOEPCA/open-science-catalog-metadata/assets/120453810/ba016cfd-ff4e-4684-b159-37cbd7165b89)

For the time being more than 270 products have been imported and made available to discover by the scientific community.

![products-stac](https://github.com/EOEPCA/open-science-catalog-metadata/assets/120453810/0b3e31c8-ce9d-4f8b-99d6-3061628be47d)

The Browser lists all products published in the Open Science Catalog, with temporal extent (start and end date of the product) provided next to the product title (in grey box). Filtering by product name is also possible.
Clicking the product will provide the main information about each item ingested into the catalog as shown in the image.

![product-page-2](https://github.com/EOEPCA/open-science-catalog-metadata/assets/120453810/4753f91b-b646-4255-a948-d2cce0b9adf0)

In the Product page the general description, metadata, access to the resource (URL link), website – URL to documentation of the product, and product extent are displayed.
Related STAC objects are linked to the corresponding files, i.e., Project, EO Mission, Variable, Theme, etc.

![metadata-product](https://github.com/EOEPCA/open-science-catalog-metadata/assets/120453810/1e8c597d-031f-4763-8a11-382f8b587c22)

The **Source metadata** is used to provide Access to **external** (source) data repository – from the data provider or the project PI and Documentation, which gives a link to the description of the product, scientific publications, etc.

Additionally search keywords are added to allow product retrieval.

In some cases, when the data is publicly available and downloadable, the access to single tiles or granules of products is being provided to the broader community. In this case another embedded STAC Catalog is created to host the spatial data itself. By selecting the catalog you can browse through single items and download one image out of vast collection of files directly from the portal.

![products-assets](https://github.com/EOEPCA/open-science-catalog-metadata/assets/120453810/b229ad19-9868-4f94-a011-1381db43661a)

The images shows the selection of a single item from a daily collection of products. Under **Assets** more information about the item can be expanded and the **Open** button allows to download the single tile to your local storage.

![metadata-assets](https://github.com/EOEPCA/open-science-catalog-metadata/assets/120453810/8cbd1bf2-1afa-4b99-80a7-13513157e7d1)

The **Up** button allows to return to the previous element in the hierarchy.

Depending on the metadata written in the single file (for example a ``.tif` or `.nc` file) additional metadata like projection or image dimensions are provided.

The next image shows an example of a Project page. Catalogs on the right panel represent Product collections associated with the given Project and discoverable from the Project page.

![project-page](https://github.com/EOEPCA/open-science-catalog-metadata/assets/120453810/ae9b723b-383a-434b-941a-9b700eaceace)

In the Project metadata a link to the corresponding EO4Society page and potentially dedicated project page built by the consortium members is additionally provided, as well as a list of consortium members and the ESA Technical Officer assigned to the project.

### Search

The STAC Browser provides client side searching directly in the browser as described above.
Additionally the static STAC files are harvested into the Resource Catalog building block provided by the EOEPCA project.
This software provides a STAC API allowing efficient searching for Products and other entries using filters on text, geospatial, temporal, and other metadata attributes.

![search](https://github.com/EOEPCA/open-science-catalog-metadata/assets/120453810/fd73379e-16f9-4649-b1db-4d55f44b8511)

The client side search offers a list of filters on the left side panel which can be applied to limit the number of products returned. Users can search by Theme, Variable, Project, EO Mission, and Region. The Region parameter can be used by drawing a user-defined shape on the interactive map, and selecting an option to filter the products by their spatial coverage, selecting only products that are either fully contained within the selected geometry, or intersecting it.

![search-1](https://github.com/EOEPCA/open-science-catalog-metadata/assets/120453810/3824063b-e89c-4906-9077-8f2d429031d0)

To add further filters, expand the given filter name with the arrow on the right and either select item(s) to filter for or type the search string to be applied.

Products that match the filters are displayed in the Results list. The number in the brackets indicates how many products match that search.

The **RESET ALL** button clears all currently applied filters and allows to start a new search.

The **EarthCODE Catalog** is integrated with the **EarthCODE Discourse forum**, making it easy for you to connect discussions directly to the resources you are exploring. This integration allows you to view or join forum discussions right from the catalog, without needing to leave the page you are on. Whether you’re exploring datasets, workflows, experiments, or other catalog items, you can view existing discussions or start new ones with just a few clicks.

## Start Discussions Directly From the Catalog

The Open Science Catalog items can be directly linked to posts in the EarthCODE Discourse forum.

![catalog](https://esa-earthcode.github.io/documentation/img/discourse/oscintegration.gif)

When browsing an item in the catalog, you’ll see a **"Start a new topic on the EarthCODE forum!"** button and a list of discussion posts linked to that particular item. This is how the Op

- **If a discussion already exists:**  
  You will be able to see all the existing comments on the same page. Clicking **"Start a new topic on the EarthCODE forum!"** will take you directly to the relevant topic in the Discourse forum, where you can join the discussion and add your comments.

- **If no discussion exists:**  
  Clicking **"Didn't find what you were looking for? Start a new topic on the EarthCODE forum!"** will create a new topic on the forum, pre-tagged with metadata from the catalog item. These tags help keep discussions organized and easily searchable.  
  > **Note:** Start discussions only on items you would like to comment on, to keep the forum focused on useful content.

By linking discussions to specific catalog items, EarthCODE ensures that all conversations related to a resource are centralized in one topic. This approach reduces redundancy, keeps the forum tidy, and makes it easier for you to find valuable insights. If needed, you can still create separate posts outside of these linked discussions. 

When commenting on a dataset, workflow, or experiment in the EarthCODE Catalog, you can make contributions to improve reusability, quality or share constructive ideas to start a conversation about the item. You could start discussions about:
- Missing or incomplete metadata (e.g. missing spatial/temporal coverage, provenance details, variable definitions)
- Feedback on data quality (e.g. unexpected values, data gaps, inconsistencies)
- Questions about the methodology used to generate the product
- Clarifications on units, data formats, or input parameters used in the experiment
- A showcase of what you've reused the experiment for
- Interesting thoughts, references, links or ideas with regards to the item
- Suggestions for improving documentation or usability
- Issues faced when trying to reproduce the experiment or reuse the data

## Standardized Metadata and Taxonomies for FAIR Data Access

Adhering by design to the "FAIR" (findable, accessible, interoperable, reproducible/reusable) principles, the Open Science Catalog aims to support better knowledge discovery and innovation. It facilitates data and knowledge integration and reuse by the scientific community. With common dictionary and unified metadata across heterogeneous sources, products discovery is facilitated. Published Products are associated to Projects and additional information is provided by tags. Themes and Variables are used as tags to facilitate Products discovery. Earth Observation Satellite Missions used to generate the Product are provided by EO-Mission description in Product's metadata.

**Themes**: One of the Earth Science topics linked to the grand science challenges set in the ESA strategy.

**Project**: Scientific research projects funded by ESA EO.

**Product**: A geoscience product representing the measured or inferred/estimated values of one or more variables over a given time range and spatial area. Products can be distinguished by geographical and temporal extent, production methodology, validation, quality, and EO Mission/sensor used to produce them.

**Variables**: Geoscience, climate, and environmental variable. Variables are represented in the hierarchical set of Earth Science variables based on the NASA GCMD keywords convention.

**Keywords**: Keywords are used to facilitate Product discovery. Based on hierarchical relationships adopted from the NASA GCMD keywords database, keywords usually refer to broader terms regarding the Variable and are assigned to a given Product.

**EO Mission**: Earth Observation Satellite Missions used to generate the Product.

![OSC-structure](https://github.com/EOEPCA/open-science-catalog-metadata/assets/120453810/8d4d4390-ec7c-40bb-9605-a02e7f33decb)


## Metrics and Statistics About the EarthCODE Catalog

### Metrics

The Open Science Catalog stores and provides also metrics and statistics on entries available for users to explore. The OSC Metrics Page provides an overview of the available geospatial Products, aggregated by either Variables (default), Themes, Projects, or EO Missions. The temporal and spatial coverage of the available Products aggregated by the selected category is displayed.

![metrics-1](https://github.com/EOEPCA/open-science-catalog-metadata/assets/120453810/25264857-1c89-45fa-b048-17d64b845968)

The slider below the metrics window
![slider](https://github.com/EOEPCA/open-science-catalog-metadata/assets/120453810/c0cb1e4f-3440-44e1-a7fb-af0fa1264218)
allows to zoom the display in and out.

Products can also be filtered using the box labeled "Search and add filter" above the metrics table. The Filters work in the same way as the Search, meaning that the Product list can be narrowed down by filtering on the Theme, Variable, Project, EO Mission, geometry, or free text search. Once selected, the filter is shown in the text box allowing to remove it and showing the currently applied filters.

![metrics-2](https://github.com/EOEPCA/open-science-catalog-metadata/assets/120453810/d42070bb-999a-4d23-8011-1cfe35f987e5)

The filter takes also free text as an input. Thus, any string typed in the filter field will be taken to search through the variable names but also their acronyms, product names, and description fields. Therefore, it is also possible to use keywords if the exact variable or product name of an item is not known. For example, the term _"carbon"_ will return the list of following variables and products _(Carbon Flux, Carbonate, Microphytoplankton Carbon, etc.)_.

![metrics-3](https://github.com/EOEPCA/open-science-catalog-metadata/assets/120453810/8dbed4f4-e41c-4fc2-808c-040b8ca3d23f)

The last column in that page provides details about the spatial coverage of selected products. Clicking on the globe icon displays the list of products and their spatial footprint.

To highlight the spatial coverage of a selected product click the pin
![pin-icon](https://github.com/EOEPCA/open-science-catalog-metadata/assets/120453810/faa609f0-bf94-4d4a-a1dc-f91f2dcc2bbb)
icon.

Click on the access
![access-icon](https://github.com/EOEPCA/open-science-catalog-metadata/assets/120453810/92d05d0e-c98b-4f6e-85f0-f3f92c1ac344)
icon to view the product page in a new tab.

![metrics-4](https://github.com/EOEPCA/open-science-catalog-metadata/assets/120453810/4244eaac-3174-4cda-81e3-dbfe3478f542)

### Statistics

Within the metrics page, the **Statistics** button is available providing a summary of the content available within the catalog.
Product statistics are provided as number of products over time, by Variable, and by EO Mission.

- Temporal coverage: A bar chart representing the number of Products per year (summary of temporal coverage of Products). Hovering over the bars shows the number of Products available in each year.

  ![stats-bar](https://github.com/EOEPCA/open-science-catalog-metadata/assets/120453810/21a06cc0-68f6-4015-b125-e6683c6bdcbd)

- Variable distribution: A list and a pie chart representing the number of products that belong to each variable and percentage in a total sum of variables available in the catalog.

  ![stats-pie](https://github.com/EOEPCA/open-science-catalog-metadata/assets/120453810/2019eec5-b706-4573-9960-fd6414fccb58)

- Satellite mission distribution: A multi-color pie chart representing the distribution of satellite missions used to generate products.

  ![stats-pie2](https://github.com/EOEPCA/open-science-catalog-metadata/assets/120453810/88e2b1d3-797d-4e9b-ad82-bbbc48771678)
