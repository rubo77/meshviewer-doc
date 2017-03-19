# Map layers

List of map layers for your meshviewer.

{% method %}
### Freifunk Regensburg Layer

Ask us friendly and you can use our layers.

| Key | Value |
| :--- | :--- |
| Recommend | yes |
| Style | simple & night |
| HTTP/2 | yes |
| Tracking | no |

{% sample lang="json" %}
```json
  {
      "name": "Freifunk Regensburg",
      // Please ask Freifunk Regensburg before using its tile server - example with retina tiles
      "url": "https://{s}.tiles.ffrgb.net/{z}/{x}/{y}{retina}.png",
      "config": {
        "maxZoom": 22,
        "subdomains": "1234",
        "attribution": "<a href=\'https://www.mapbox.com/about/maps/\' target=\'_blank\'>&copy; Mapbox</a> <a href=\'https://openstreetmap.org/about/\' target=\'_blank\'>&copy; OpenStreetMap</a> <a class=\'mapbox-improve-map\' href=\'https://www.mapbox.com/map-feedback/\' target=\'_blank\'>Improve this map</a>",
        "start": 6
      }
    },
```

#### Night style

{% sample lang="json" %}
```json

    {
      "name": "Freifunk Regensburg Night",
      // Please ask Freifunk Regensburg before using its tile server - example with retina and dark tiles
      "url": "https://{s}.tiles.ffrgb.net/n/{z}/{x}/{y}{retina}.png",
      "config": {
        "maxZoom": 22,
        "subdomains": "1234",
        "attribution": "<a href=\'https://www.mapbox.com/about/maps/\' target=\'_blank\'>&copy; Mapbox</a> <a href=\'https://openstreetmap.org/about/\' target=\'_blank\'>&copy; OpenStreetMap</a> <a class=\'mapbox-improve-map\' href=\'https://www.mapbox.com/map-feedback/\' target=\'_blank\'>Improve this map</a>",
        "mode": "night",
        "start": 19,
        "end": 
      }
    }
```
{% endmethod %}

{% method %}
### OpenStreetMap FR - Hot style

{% sample lang="json" %}
```json

    {
      "name": "OpenStreetMap.HOT",
      "url": "https://{s}.tile.openstreetmap.fr/hot/{z}/{x}/{y}.png",
      "config": {
        "maxZoom": 19,
        "attribution": "&copy; Openstreetmap France | &copy; <a href=\"http://www.openstreetmap.org/copyright\">OpenStreetMap</a>"
      }
    }
```
{% endmethod %}

{% method %}
### HERE Map

{% sample lang="json" %}
Requries API token - free account with limited views available.

```json

    {
      "name": "HERE",
      // Please use your own API key - Free plan is on right side after the pay plans
      "url": "https://{s}.base.maps.api.here.com/maptile/2.1/maptile/newest/normal.day/{z}/{x}/{y}/256/png8?app_id=YOUR_KEY&app_code=YOUR_CODE&lg=deu",
      "config": {
        "attribution": "Map &copy; 1987-2014 <a href=\"http://developer.here.com\">HERE</a>",
        "subdomains": "1234",
        "maxZoom": 20
      }
    }
```
{% endmethod %}

{% method %}
#### Satellite hybrid View

{% sample lang="json" %}
```json
    {
      "name": "HERE.hybridDay",
      // Please use your own API key - Free plan is on right side after the pay plans
      "url": "https://{s}.aerial.maps.api.here.com/maptile/2.1/maptile/newest/{variant}/{z}/{x}/{y}/256/png8?app_id=YOUR_KEY&app_code=YOUR_CODE&lg=deu",
      "config": {
        "attribution": "Map &copy; 1987-2014 <a href=\"http://developer.here.com\">HERE</a>",
        "subdomains": "1234",
        "variant": "hybrid.day",
        "maxZoom": 20
      }
    }
```
{% endmethod %}

{% method %}
### Satellite map

{% sample lang="json" %}
```json

    {
      "name": "Esri.WorldImagery",
      "url": "//server.arcgisonline.com/ArcGIS/rest/services/World_Imagery/MapServer/tile/{z}/{y}/{x}",
      "config": {
        "maxZoom": 20,
        "attribution": "Tiles &copy; Esri &mdash; Source: Esri, i-cubed, USDA, USGS, AEX, GeoEye, Getmapping, Aerogrid, IGN, IGP, UPR-EGP, and the GIS User Community"
      }
    },
    ```
{% endmethod %}