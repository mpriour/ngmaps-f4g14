# OpenLayers

---

1. angular-openlayers-directive

  * OL3 Only
  
  * Script style
  
  * Same person as angular-leaflet-directive
  
  * <https://github.com/tombatossals/angular-openlayers-directive/>

2. angular-openlayers

  * OL2 Only
  
  * Declarative style
  
  * <https://github.com/qorsmond/angular-openlayers/>

---

## angular-openlayers-directive

```

<body ng-controller="DemoZoomLevelController">
      <openlayers center="london" layers="layers" height="400px"></openlayers>
</body>

```

```

app.controller('DemoZoomLevelController', 
[ "$scope", function($scope) {
  angular.extend($scope, {
      london: {
          lat: 51.505,
          lon: -0.09,
          zoom: 10
      },
      layers: {
          main: {
              type: "OSM"
          }
      }
  });

```

---
