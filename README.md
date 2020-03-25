# User Activity Map
This User Activity Map is visualization of statistics data about user visits and downloads of items in DSPace-CRIS. This map can be merged to the repository and display data in real time. 


### What features
Leaflet map

displaying visitor's information
 * links to viewed item and collection
 * Item views in past month
 * Total Views
 * Monthly Views (current month + 3 past months)
 * Total Downloads
 * Total Items

auto mode (automatic display)
manual mode (pause, forward, backward)


## How to install
 * Clone the repositiory from github website
 * Merge the branch to DSpace-CRIS project, or manually add all changes to DSpace-CRIS
 * Register to leaflet for access token (https://docs.mapbox.com/help/glossary/access-token), put token to dspace.cfg (jspui.leaflet.accesstoken=YOUR_MAPBOX_ACCESS_TOKEN)
 * Rebuild DSpace-CRIS 

## How to run
Set up time-based job scheduler using cron to run periodically to update map information

The example of scheduler see as below:
Run solr export every 15 mins
```
 */15 * * * * $DSPACE/bin/solr-export &> /dev/null
```

Run processing solr data every 15 mins

```
 1,16,31,46 * * * * $DSPACE/bin/dspace geo-solr-export
```

### License

MIT

### Author Information

Developed and maintained by John Zhang and Yang Le (yanglegd@gmail.com)
