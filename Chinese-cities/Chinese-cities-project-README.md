# Chinese cities

Harvard Map Collection and ITS staff devised this project to give increased online visibility to about 350 maps of Chinese cities from the Harvard Digital Collections. Maps of China are frequently requested by visiting researchers to the Map Collection, and images of them are increasingly requested for publication.

As described in the [Tasks section of the WikiProject page](https://www.wikidata.org/wiki/Wikidata:WikiProject_Linked_Data_for_Production/Scanned_Maps_in_Wikimedia_Commons_and_Wikidata_Project#Tasks), there were various steps to gathering the data and converting the data. The files and code snippets in this folder comprise the work that was done to make those steps happen.

1. Batch conversion of MARCXML bibliographic descriptions to Wikidata entities / Structured data on the Commons
  * Alma analytics to identify and export set of map image records as MARCXML
  * MarcEdit to OpenRefine conversion
  * OpenRefine reconciliation of MARC data to Wikidata entities for titles, contributors, publisher, place names, etc.
2. Batch conversion of MARCXML authority descriptions to Wikidata entities / Structured data on the Commons
  * Alma analytics to identify and export set of map-related name entities as LCNA MARCXML
  * OpenRefine reconciliation of LCNA data to Wikidata entities
  * Wikidata modeling and, possibly, Cradle form creation for map and cartographer entities
3. Manual creating/editing of Wikidata/Commons cartographer/contributor entities
  * Enhance minimal or non-existent descriptions with library paper data sources, e.g. Dictionary of Map Makers
4. Manual editing of Wikidata/Commons map image descriptions
  * Describe map components (e.g. decorative cartouche and vignette depictions, and other non-cartographic entities)
  * Host mini Edit-a-thon
