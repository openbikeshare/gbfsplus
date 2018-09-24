# GBFS+ | General Bike Share Feed Specification Plus
To accommodate smart bike sharing in The Netherlands and elsewhere

## Preface
Twelve Dutch organisations have the ambition to create an open standard for bike sharing in The Netherlands. The Ministry of Infrastructure and five big cities (Amsterdam, Rotterdam, Utrecht, The Hague, Eindhoven) stimulate this initiative because it has huge benefits for society. CROW/Fietsberaad also promotes this initiative to establish an open standard.

We decided to start with the American GBFS open standard and modify and extend it according to our needs. We make proposals for those changes in a fork of GBFS, we refer to it as GBFS+, https://github.com/openbikeshare/gbfs. We will try feeding these modifications back into the original GBFS, by doing change requests, if we can't come to a agreement about new functionality with the maintainers of GBFS we will stick to our own profile. We decided to define and use the following open standard:

## The standard: GBFS+ 

1. __GBFS__ 
We will use the GBFS specification (latest version), we make extensions on the current specification, we use GBFS+ in this document to refer to this extensions.

2. __Deep links, Add rental_url to free bikes and stations__
There is already a change-requests (from others) for an extension of the standard, covering exactly our wishes. So we include request #25 in GBFS+, which enables deep links.

3. __Type_of_system__
We will add type_of_system in the “system info” file. Allowed values are [free_floating, station_based, virtual_station_based]

4. __Type_of_bike__
We add a file “Types_of_bikes” which describes the different bike types (type_id, name, gears, electric, description, img_url)
In free-bike-status file we add the field type_of_bike
(our first proposal on OpenBikeShare Github)  

5. __TTL__
The time to live (TTL) for real-time data feeds will be at most 30s, so that traveller has always the most actual information about the availability of bicycles.

## Recommendations
* There are some other topics to cover to make an awesome bike standard in the future, but more research has to be done. Possible topics are:
Which fields should be compulsory?
* Operation area: For a free-floating system we would like to indicate where you can return your bike (for example you are only allowed to return the bike within the city). In this https://github.com/NABSA/gbfs/issues/65 thread there is already a discussion about this idea.
* Virtual stations: We would like to introduce virtual stations (a virtual location where you allowed to park your bike) within GBFS so operators comparable with Donkey Republic are supported as well. We created a proposal. The exact location of a virtual zone should be presented as GeoJSON polygon in station_information.json.
 