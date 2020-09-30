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

## Postprocessing steps

Wikidata items and their Wikimedia Commons images that have been successfully loaded can be viewed in the [Queries](https://www.wikidata.org/wiki/Wikidata%3AWikiProject_Linked_Data_for_Production%2FScanned_Maps_in_Wikimedia_Commons_and_Wikidata_Project#Queries) section of the WikiProject page.

Steps 3 and 4 listed above can be expanded into the following tasks. These do not have to be accomplished sequentially.

*	Spot check the completed map images in the [Old Maps of China in Harvard Map Collection](https://commons.wikimedia.org/wiki/Category:Old_maps_of_China_in_Harvard_Map_Collection) Wikimedia Commons category for duplicates, multi-sheet images that need to be disambiguated, or other issues that need additional explanation in the file information.
*	Go back to the list of Wikidata items in the Queries section, and see if there are any images for them remaining in Harvard Library's [Scanned Maps](https://curiosity.lib.harvard.edu/scanned-maps) Digital Collections that weren't loaded before. Also consider using open images from other libraries for anything not found.
*	Modify the Commons images' authors and publishers with Creator templates, where applicable, or at least a Wikidata/Wikipedia linked name for the author and publisher. For example, type [{{Creator:John Speed}}](https://commons.wikimedia.org/wiki/Creator:John_Speed) into the Author section of [_The kingdome of China_](https://commons.wikimedia.org/wiki/File:The_kingdome_of_China_1626_22088634.jpg) instead of just the text "John Speed."
*	Add at least English-language captions to Commons images. Translated captions in Chinese, Japanese, and Russian would also be great to crowdsource.
*	Add Structured Data to Commons images. The preferred starting points would be using the default _depicts_ statement, along with adding the _digital representation of_ statement, and using the map Wikidata item as the value for each. You can use the new [Commons Query Service](https://commons.wikimedia.org/wiki/Commons:SPARQL_query_service/queries/examples) to see which files on the project list don’t have statements yet: https://tinyurl.com/y37x7np7
*	Add all the images to their respective Wikidata items in the _image(P18)_ statement. This could potentially be done with QuickStatements, or even [TABernacle](https://tabernacle.toolforge.org/#/tab/sparql/SELECT%20%3Fitem%20WHERE%20%7B%0A%20%3Fitem%20wdt%3AP5008%20wd%3AQ99360079.%0A%20%7D/P31%3BLen%3BDen%3BAen).
*	Crowdsourcing option: encourage people to add [image annotations](https://commons.wikimedia.org/wiki/Help:Gadget-ImageAnnotator), either as stand-alone descriptive notes or [to add Structured Data to specific pixel regions](https://wd-image-positions.toolforge.org/).
* MOST IMPORTANT CROWDSOURCING OF ALL: encourage people to add images to Wikipedia page. The difference in page views is eyewatering. See the [Bamglama Analytics](https://glamtools.toolforge.org/baglama2/#gid=530&month=202008&giu=enwiki&server=en.wikipedia.org) for the Harvard Map Collection category, plus the more granular [Pageviews Analysis](https://pageviews.toolforge.org/?project=en.wikipedia.org&platform=all-access&agent=user&redirects=0&start=2020-08-01&end=2020-08-31&pages=Harz) native to Wikipedia pages.
