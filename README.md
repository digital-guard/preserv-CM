# preserv-CM
[Digital preservation](https://en.wikipedia.org/wiki/Digital_preservation) of the main sources of the **AddressForAll-Cameroonian database**, maintained by the [AddressForAll Institute](http://addressforall.org/).

To Cameroon was assigned: in the [ISO&nbsp;3166](https://en.wikipedia.org/wiki/ISO_3166) context the geocode [**CM**](https://en.wikipedia.org/wiki/ISO_3166-2:CM) and the number [**120**](https://en.wikipedia.org/wiki/ISO_3166-1_numeric); in [Wikidata](https://wikidata.org) the identifier [Q1009](http://wikidata.org/entity/Q1009); in [OpenStreetMap](https://osm.org) the [*relation* id 192830](http://osm.org/relation/192830).

## Territorial organization
The national territory and its subdivisions represent *jurisdictions*:

* The country is divided into *10 regions* (then-provinces), semi-autonomous, that are headed by a governor appointed by the president of the republic.
The geocodes of the regions follow the convention registered by ISO 3166-2:CM. In OpenStreetMap it is agreed that the subdivision by regions corresponds to administrative level 4.

* The regions are subdivided into *58 departments* that are headed by divisional officers (_préfets_) appointed by the president of the republic.

* The departments are subdivided into communes (_arrondissements_) that are headed by assistant divisional officers (_sous-prefets_).

* The communes are subdivided into districts that are headed by district heads (_chefs de district_).

The urban cadastres are found in the communes. [CONFIRM?]

The jurisdiction that assigns names to streets and the urban numbering system is the commune. [CONFIRM?]

## Organization of this repository
In this _git_, only metadata is saved, that is, entity descriptors such as names and geocodes — maps and other data, stored externally because they are very large. The metadata was organized as follows, in the [`/data`](./data) folder:

* [`/data`](./data): original **input** data, that is, metadata provided for the system.
   * `jurisdictionLevel*.csv`: jurisdictions (at all levels) and their geocodes. The first subdivision is [jurisdictionLevel4.csv](./data/jurisdictionLevel4.csv).
   * [`donor.csv`](./data/donor.csv): data package donors. Metadata of the institutions that provide official data.
   * [`donatedPack.csv`](./data/donatedPack.csv): descriptors of the donated files.
   * *packages* (`_packXX` folders): *hash*  and other externally stored file descriptors, as well as `makefile` and other process descriptors to decompress these files and take them to the database (PostregSQL)...

* [`/data/_out`](./data/_out): system-generated results (**output**), that is, metadata created from the algorithms and statistics applied to the `_pack` data.

## License
[License CC0](https://creativecommons.org/publicdomain/zero/1.0/deed.en).
