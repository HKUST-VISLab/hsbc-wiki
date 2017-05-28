## Database: geo_maps
This database is designed to store geo-based information like the street, node, regions.

- osm_node
- osm_way
- osm_highway
- hk_node
- hk_link

***
### osm_node
Nodes are used to define a standalone geo-points in the map. Some of the nodes have special meaning like the crossroad or postbox, while some other points only defined for the purpose to describe a street. 
Ref: http://wiki.openstreetmap.org/wiki/Node

  * _id: an object id created by mongodb
  * id: string, an unique id for all ndoes assigned by the osm system
  * location: two elements array([lat, lon], lat, lon: float), the location of the node
  * tag: description of node(k-v pairs, k and v are unicode string), the tag main contains
    

an example
>      {
>          "_id" : ObjectId("59145f9ae177d259648c7fc6"),
>          u 'id': u '24330691',
>          u 'location': [22.350627, 114.1849161]
>          u 'name:en': u 'Hong Kong',
>          u 'ref:en': u 'HK',
>          u 'is_in:country': u 'China'
>      }

***
### osm_way
A way is an ordered list of nodes, it could be a region or a street. 
Ref: http://wiki.openstreetmap.org/wiki/Way

  * _id: an object id created by mongodb
  * id: string, an unique id for all way assigned by the osm system
  * ng: [ref], ref is the id of nodes(osm_node.id)
  * tag: description of node(k-v pairs, k and v are unicode string), the tag main contains

an example
>      {
>          u '_id': ObjectId('5929848c038f304e04bf2466'),
>          u 'id': u '4181592',
>          u 'nd': [u '253333910', u '3304026514', u '2291194554'],
>          u 'tag': {
>		       u 'bridge': u 'yes',
>		       u 'layer': u '1',
>		       u 'name:en': u 'MTR Airport Express',
>		       u 'name': u '\u6e2f\u9435\u6a5f\u5834\u5feb\u7dab MTR Airport Express',
>		       u 'start_date': u '1998-07-06'
>	       }
>      }

### osm_highway
A highway is an ordered list of nodes, used for identifying any kind of road, street or path. 
Ref: http://wiki.openstreetmap.org/wiki/Key:highway

  * _id: an object id created by mongodb
  * id: string, an unique id for all way assigned by the osm system
  * ng: [ref], ref is the id of nodes(osm_node.id)
  * tag: description of node(k-v pairs, k and v are unicode string), the tag main contains

an example
See the example of way

### hk_node
All the nodes used for the "TRAFFIC SPEED MAP", the description can be found in Ref1 and the raw data can be found in Ref2
Ref1: https://data.gov.hk/en-data/dataset/hk-td-tis-traffic-speed-map
Ref2: http://www.gov.hk/en/theme/psi/datasets/tsm_link_and_node_info_v2.xls
Ref2: https://data.gov.hk/en/datagovhk-api/coordinate-conversion

  * _id: an object id created by mongodb
  * id: string, an unique id for all nodes in the tsm system
  * hk80: hk1980 coordinates[northings, eastings], the methods transform hk80 to gps can be found in Ref3  
  * position: the corresponding gps results

an example
See the example of way
>      {
>            "_id" : ObjectId("592a4619038f3082303a4620"),
>            "position" : [22.28599503, 114.155241726],
>            "id" : "722",
>            "hk80" : ["816345.067", "834038.674"]
>      }

### hk_links
All the links used for the "TRAFFIC SPEED MAP", the description can be found in Ref1 and the raw data can be found in Ref2
Ref1: https://data.gov.hk/en-data/dataset/hk-td-tis-traffic-speed-map
Ref2: http://www.gov.hk/en/theme/psi/datasets/tsm_link_and_node_info_v2.xls
Ref2: https://data.gov.hk/en/datagovhk-api/coordinate-conversion

  * _id: an object id created by mongodb
  * id: string, an unique id for all links in the tsm system
  * source: string, the id of source node
  * source_position: [lat, lon], the gps position of source node  
  * target: string, the id of target node
  * target_position: [lat, lon], the gps position of target node  
  * region: string, the region of the link: (HK – Hong Kong, K – Kowloon, TM – Tuen Mun, ST – Sha Tin)
  * type: string, the type of road(MAJOR ROUTE – Refers to roads with speed limit of 70km/h or above; URBAN ROAD – Refers to roads with speed limit of 50 km/h )


an example
See the example of way
>      {
>            "_id" : ObjectId("592a4619038f3082303a4620"),
>            "id" : "722-50059"
>            "source" : "722",
>            "source_position" : [ 22.28599503, 114.155241726],
>            "target" : "50059",
>            "target_position" : [22.286866123, 114.15353399],
>            "region" : "HK",
>            "type": "MAJOR ROUTE",
>      }

