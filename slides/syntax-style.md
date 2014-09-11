# Directive Syntax

## 2 Styles

* Declarative - most simple user options & handlers go in markup

* Script - only pointers to scope properties in markup

---

## Declarative

```

<div leaflet-map controls="layers">
	<az-layer name="Street" lyr-type="tiles" lyr-options="{isBaseLayer:true}"></az-layer>
	<az-layer name="Aerial" lyr-type="tiles" lyr-url="http://otile{s}.mqcdn.com/tiles/1.0.0/sat/{z}/{x}/{y}.png"
		is-base-layer="true"></az-layer>
	<az-layer name="Radar"  lyr-type="wms" lyr-url="http://gis.srh.noaa.gov/ArcGIS/services/Radar_warnings/MapServer/WMSServer"
		layers="0,1" version="1.3.0" crs="EPSG:102100" transparent="true" opacity="0.75"></az-layer>
	<az-layer name="Airports" lyr-type="geojson" lyr-url="examples/data/airports.json"></az-layer>
</div>

```

---

## Script

```
<div ng-controller="MarkerController">
    <leaflet markers="markers" center="osloCenter"></leaflet>
</div>

```

```

app.controller("MarkerController", [ '$scope', function($scope) {
    angular.extend($scope, {
        osloCenter: {
            lat: 59.91,
            lng: 10.75,
            zoom: 12
        },
        markers: {
            osloMarker: {
                lat: 59.91,
                lng: 10.75,
                message: "I want to travel here!",
                focus: true,
                draggable: false
            }
        },
        defaults: {
            scrollWheelZoom: false
        }
    });
}]);

```

