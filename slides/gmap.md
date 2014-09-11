# Google Maps

---

1. angular-google-maps
  * <https://angular-ui.github.io/angular-google-maps/>
  * Script style

2. ngmap
  * <https://github.com/allenhwkim/angularjs-google-maps/>
  * Declarative style

---

## angular-google-maps

```
<div id="map_canvas" >
    <google-map center="map.center" zoom="map.zoom">
        <marker coords="map.marker.coords" idkey="map.marker.id" options="map.marker.options"></marker>
    </google-map>
</div>

```

```
  $scope.map = {
      center: {
          latitude: 35.027469,
          longitude: -111.022753
      },
      zoom: 4,
      marker: {
          id:0,
          coords: {
              latitude: 35.027469,
              longitude: -111.022753
          },
          options: {
              icon: {
                  anchor: new google.maps.Point(36,36),
                  origin: new google.maps.Point(0,0),
                  scaledSize: new google.maps.Size(72,72),
                  url: 'assets/images/cluster1.png'
              }
          }
      }
  };

```


---


## ngmap

```
<map zoom="11" center="[40.74, -74.18]">
  <marker position="Toronto Canada" 
          title="You are here" 
          animation="Animation.BOUNCE" 
          centered="true">
  </marker>
</map>

```

---