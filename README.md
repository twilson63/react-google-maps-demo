# Demo React Google maps

- Setup API Credentials

- Add SCRIPT Tag to your head

```
<script src="https://maps.googleapis.com/maps/api/js?key=[Your Key]"></script>

```

- Install from npm

`npm install react-google-maps@beta`


- Create a Higher Order component

```
const GettingStartedGoogleMap = withGoogleMap(props => (
  <GoogleMap
    ref={props.onMapLoad}
    defaultZoom={3}
    defaultCenter={{ lat: -25.363882, lng: 131.044922 }}
    onClick={props.onMapClick}
    >
    {props.markers.map((marker, index) =>
      <Marker {...marker} />
    )}
  </GoogleMap>
))
```

---

- Call the component


```
<GettingStartedGoogleMap
  containerElement={
    <div style={{ height: '400px' }} />
  }
  mapElement={
    <div style={{ height: '400px' }} />
  }
  onMapLoad={() => null }
  onMapClick={() => null }
  markers={[{
    position: {
      lat: 25.0112183,
      lng: 121.52067570000001,
    },
    key: `Taiwan`,
    defaultAnimation: 2,
  }]}
  onMarkerRightClick={() => null }
  >
</GettingStartedGoogleMap>
```
