## FAIR may be necessary, but is not sufficient

I looked at the [Demographics of Police Stops](https://open-data.bouldercolorado.gov/datasets/1f850e90d27a4bf58d5b66405d59045f_0/explore) data set from the [Boulder Open Data](https://open-data.bouldercolorado.gov/) portal.

Thinking about this data set with the FAIR guiding principles is interesting. The data set has been published in a way that satisfies much of what we’re looking for, and also is not usable in many ways..

The city’s open data presentation hub is easy to search and navigate. It is possible to preview the data for larger data sets, such as [the tree survey](https://open-data.bouldercolorado.gov/datasets/dbbae8bdb0a44d17934243b88e85ef2b_0/explore?location=40.021295%2C-105.274635%2C17.00), without downloading, and the data sets are presented in a structured and consistent way.

The data are **F** findable \- each stop has a unique identifier, which should allow for matching stop demographics with [stop outcomes](https://open-data.bouldercolorado.gov/search?bbox=-105.34223999999996%2C%2039.95274000000004%2C%20-105.21623999999996%2C%2040.07874000000006). The open data site, hosted on or designed with [ArcGIS Hub](https://hub.arcgis.com/), is set up to include easy-to-find information about data types, the license, and the size of the data set. A summary explains the data set and includes links to a data dictionary and a methodology PDF.

If you choose to download the data, you’re given a choice of formats, including some options that are intended for geographic data and make less sense here. It is relatively **A** accessible to be able to choose between getting an Excel or a CSV version, depending on your use or technological setup.

The data are **R** reusable in that there is a clear license ([CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/)), which they link to for greater clarity. 

The concerns I have with this data set are more about how it was created than how it was published, though they are connected.

The published date indicated is August 27, 2020, so I was already curious about why the data were not being updated more frequently. Looking at the data set, all of the stops are between December 2017 and December 2018, which is extremely limited.

The [methodology document](https://webappsprod.bouldercolorado.gov/opendata/methods_police_stop_data.pdf) makes me even more sceptical, as for “race and ethnicity information, officers record this information based on their perception of the individual.” Additionally, some of the cleaning the methodology document mentions, such as filtered out improbable birth years, does not seem to have happened, as more than one stop is recorded for someone born after 2900\.

I appreciate the efforts of cities and states to make data more available, but there are ways in which this data set in particular feels like FAIR washing. The portal is cleanly designed, the data is structured, we get a data dictionary and an explanation of how the data set was created. At the same time, the data is based on the perceptions of the police officer filling in a module (I suppose the perceived demographics are pretty important in this situation, but it still feels like a less-than-ideal system to me), and is for one year almost a decade ago. The data are reusable by how they’re licensed, but might not make sense to be depended on. It wouldn’t work with the acronym, but I’d rather this data was more **W** worthwhile.
