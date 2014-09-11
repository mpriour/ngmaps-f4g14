#  leaflet

---

## angular-leaflet-directive

* Script style

* inspired by angular-google-maps

<http://tombatossals.github.io/angular-leaflet-directive/>

---

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
