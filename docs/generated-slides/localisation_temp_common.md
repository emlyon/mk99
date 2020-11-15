= Localization and value creation

Clément Levallois <levallois@em-lyon.com>
2017-31-07

last modified: {docdate}

:icons!:
:iconsfont:   font-awesome
:revnumber: 1.0
:example-caption!:

:title-logo-image: EMLyon_logo_corp.png[width="242" align="center"]

image::EMLyon_logo_corp.png[width="242" align="center"]
{nbsp} +

//ST: 'Escape' or 'o' to see all sides, F11 for full screen, 's' for speaker notes


== 1. Localization brings interesting new dimensions

//ST: !
Localization relates activities to physical space, in at least 4 different ways:

//ST: !
Place: Where is this activity happening?

//ST: !
Distance: Are these two agents neighbors?

//ST: !
Movement: Is this agent travelling?

(together with *speed* and *acceleration*)

//ST: !
Structure: How are these agents and activities *configured* in space?


//ST: !
=== a. Example - Facebook Local Awareness Feature

//ST: !
image::fb-aware.png[align"center", title="Facebook Local Awareness Ad Feature"]
{nbsp} +

//ST: !
“Helping Local Businesses Reach More Customers”:

- Target ads to people living in a radius around your store.
- Can also target people who have been recently in this radius.

-> https://www.facebook.com/business/learn/facebook-create-ad-reach-ads

//ST: !
video::-YE90ygswoU[youtube]

//ST: !
=== b. Example - Placemeter

//ST: !
image::placemeter.png[align"center", title="Placemeter analyzes pedestrian traffic through video"]
{nbsp} +

//ST: !
“Using computer vision to analyze real life activity”:

- Cameras placed in public places (possibly at the windows of private households)
- Video is treated on the device attached to the camera, not saved.
- measures pedestrian traffic in front of stores to provide "main street analytics"

-> https://www.placemeter.com/

//ST: !
video::irydHrRdpkY[youtube]

//ST: !
=== c. Example - Data @GrandLyon

//ST: !
https://data.grandlyon.com/[
image:logo-smart-data-grand-lyon.png[align"center", title="Grand Lyon Data"]]

//ST: !
An initiative by the city of Lyon

-> Making data open to foster innovation for citizens and businesses

-> Includes many datasets with geographical relevance

//ST: !
Similar initiatives in large cities:

https://data.amsterdam.nl/[image:amsterdam.gif[width=150]]
https://www.beijingcitylab.com/[image:bjcitylab.jpg[width=150]]
http://www.milanosmartcity.org/joomla/[image:milano.jpg[width=150]]
http://smartcity.jakarta.go.id/[image:jakarta.png[width=150]]
http://smartcityinnovationlab.com/[image:lisboa.png[width=150]]

== 2. The visual power of maps

//ST: !
=== a. Map: useful metaphors with a political dimension

//ST: !
- The visual metaphor of the map is widely understood

- Makes exploration easy: all visible at once, while zoom allows for details as well

- Multiple information cues (colors, symbols, shapes, layers, etc.)


//ST: !
- Keep in mind: maps are always *political*

- Watch this extract from the TV series "The West Wing“, Season 2, Episode 16:

//ST: !
video::vVX-PrBRtTY[youtube]

//ST: !
=== b. Example: how to explore the real estate market in the Netherlands

//ST: !
- Every single building of the Netherlands on a map
- Colored by year of construction
- With role (retail or housing?) and surface highlighted
- Zoomable and draggable

//ST: !
http://code.waag.org/buildings/[image:waag.png[align"center", title="Visual exploration of real estate in NL"]]

//ST: !
=== c. Key resources to work with maps

//ST: !
image::stamen.jpg[align="center", title="Stamen Design"]
{nbsp} +

- Agency based in San Francisco
- Famous for cutting research in map design

//ST: !
image::mapbox.png[align="center", title="MapBox"]
{nbsp} +

- Mapbox.com
- SaaS to create interactive maps in web pages and mobile apps.

//ST: !
image::openstreetmap.png[align="center", title="Openstreetmap"]
{nbsp} +

- OpenStreetMap
- A crowd sourced open source map of the world. Available through API.


== 3. How to represent “space” in data format?

//ST: !
=== a. The specifity of geospatial data
//ST: !

Data is traditionally stored in tables in relational databases, taking this form:

image::table-example.png[align="center", title="A table with two entries"]
{nbsp} +

//ST: !
A table can have millions of rows. How to retrieve information such as "get all customers living in Rotterdam"?

"SQL" (Structured Query Language) is a system to express these kinds of queries.

//ST: !
In the table shown above, a query written in SQL look in the "Address" column and inspect all the text to find if "Rotterdam" is present or not.

//ST: !
This is highly inefficient (slow), and more complex queries would not work.

For example, the table above could not be queried for "get all customers living in a 10 miles radius around Rotterdam".

//ST: !
So how to store ((geospatial data)) in a way that makes it easy to retrieve?

//ST: !
=== b. Solutions to store and retrieve geospatial data

//ST: !
1. SQL solutions

Even if SQL does not perform well on geospatial data "out of the box", extra modules have been developed to deal with it.

//ST: !
Microsoft SQL server since 2008:

- Possible to store and query “geometric” and “geographic” objects
- Possible to use complex queries on these objects

//ST: !
[start=2]
2. NoSQL (((SQL vs NoSQL))) solutions

Since ~ 2005, new types of databases have been developed, which don't follow a table structure in order to facilitate the query of special kinds of data, like geospatial data or network data.

These new databases are called "NoSQL databases"

//ST: !
image::carto.png[align="center", title="the Carto Platform"]
{nbsp} +

https://carto.com/[Carto (ex CartoDB)]: specializing in geospatial data + mapping.

//ST: !
image::neo4j.png[align="center", title="Neo4J, a database for networks"]
{nbsp} +

http://neo4j-contrib.github.io/spatial/[Neo4J Spatial] enables to mix the logics of networks with places in the data, so that you can make such queries on your data:

"Select all streets in the Municipality of NYC where at least 2 of my friends are walking right now."

//ST: !
image::topojson.png[align="center", title="GeoJSon and TopoJSon are derivations of the json formats for geospatial data"]
{nbsp} +

GeoJSon and TopoJSon: 2 data formats to represent geometric and geographic data developed for Javascript applications – and beyond.

== 4. Two friends for localization: personalization and real-time

//ST: !
Knowing the person, its location, at a precise time unlocks meaningful push notifications

//ST: !
Push notifications are these alerts sent by an app on your mobile, visible as transient icons.

//ST: !
Gets “push marketing” back on solid foundations:

Push marketing actions only to the right person, at the right place, at the right time (and at the right frequency!)

== 5. Ending with a provocation: Challenging the usefulness of location

//ST: !
=== a. Localization is about people and __territories__
//ST: !
- Data is a fungible and universal material (just 0s and 1s)

- Geographical coordinates are perfectly universal (just need a longitude and latitude)

and yet …

//ST: !
The logic of territories is shaping data: there is a geography of data.

Cultural, social, political, linguistic, economic dimensions to data.

-> representations with a supposedly universal and transparent coordinate system blinds us to this fact.

//ST: !
This argument is made by Frederic Martel (((Martel, Frederic))) in his book "Smart": Internet does not flatten everything into one big model. There are several Internets with their geography, politics and sociology.

//ST: !
https://www.amazon.com/s/ref=nb_sb_noss?url=search-alias%3Daps&field-keywords=smart+frederic+martel&rh=i%3Aaps%2Ck%3Asmart+frederic+martel[image:smart.jpg[align="center", title="Smart by Frederic Martel"]]

//ST: !
- Data protection: http://www.darkreading.com/cloud/privacy-security-and-the-geography-of-data-protection-/a/d-id/1315480[not all countries are equal]

//ST: !
- Data handling devices

India and Africa  have ++ share of mobile devices

//ST: !
- Data production

*Amazon Mechanical Turk* (((Amazon, Amazon Mechanical Turk))) is a service of data production through the hiring of a distributed crowd of workers. Tends to "erase distance".

Yet, the geographical distribution of workers on Amazon Mechanical Turk is far from even. The following figure is taken  http://aclweb.org/anthology/Q14-1007[from this study]:

//ST: !
image::amt-distribution.png[align="center", title="Distribution of Amazon Mechanical Turk workers"]
{nbsp} +


//ST: !
=== b. Distributed systems – the end of territories?

//ST: !
The libertarian dream of the cypher-punks: individuals transact without consideration for their nationality, currency, legal system, political regime.

//ST: !
Organizations, banking, voting systems, … any aggregated human activity could emerge without reference to local territories or institutions. Just groups of individuals transacting voluntarily and securely, without a notion of place or distance.

//ST: !
- Bitcoin: the currency for these transactions?
- Torrent: The exchange platform for numeric goods?
- Ethereum: the platform where contracts are made and executed?

//ST: !
https://www.amazon.com/This-Machine-Kills-Secrets-Whistleblowers/dp/0142180491/ref=sr_1_1?ie=UTF8&qid=1508079962&sr=8-1&keywords=this+machine+kills+secrets[image:cypherpunks.png[align="center",title="This machine kills secrets by Andy Greenberg"]]

== The end
//ST: !

Find references for this lesson, and other lessons, https://seinecle.github.io/mk99/[here].

image:round_portrait_mini_150.png[align="center", role="right"]
This course is made by Clement Levallois.

Discover my other courses in data / tech for business: https://www.clementlevallois.net

Or get in touch via Twitter: https://www.twitter.com/seinecle[@seinecle]
_portrait_mini_150.png[align="center", role="right"]
This course is made by Clement Levallois.

Discover my other courses in data / tech for business: http://www.clementlevallois.net

Or get in touch via Twitter: https://www.twitter.com/seinecle[@seinecle]
