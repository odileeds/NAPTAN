# NAPTAN

Adding geography to all the bus stops in the [NAPTAN dataset](https://www.travelinedata.org.uk/other-transport-open-data/transport-stops/).

## Method

We used [QGIS](https://www.qgis.org/en/site/) to add [ONS codes](https://en.wikipedia.org/wiki/ONS_coding_system) to every NAPTAN bus stop for various geographies including:

  * [Wards](http://geoportal.statistics.gov.uk/datasets/wards-may-2018-uk-bgc) (`wd18cd`)
  * [Westminster Parliamentary Constituencies](http://geoportal.statistics.gov.uk/datasets/westminster-parliamentary-constituencies-december-2017-full-extent-boundaries-in-great-britain) (`pcon17cd`)
  * [Local Authority](http://geoportal.statistics.gov.uk/datasets/local-authority-districts-december-2017-full-extent-boundaries-in-united-kingdom-wgs84) (`lad17cd`)
  * [Upper Tier Local Authority](http://geoportal.statistics.gov.uk/datasets/upper-tier-local-authorities-december-2011-boundaries) (`utla11cd`)
  * [NUTS3 region](http://geoportal.statistics.gov.uk/datasets/nuts-level-3-january-2018-full-extent-boundaries-in-the-united-kingdom) (`nuts318cd`)

The original NAPTAN data already included output area codes.

The NAPTAN data were added as a "Delimited Text Layer". The Shapefiles for each geography type were downloaded from the ONS Geoportal and included as layers. The attribute tables for each geography were added to the bus stops dataset using `Vector->Data Management Tools->Join attributes by location`. The final layer was then saved as a CSV file with a limited set of columns included.