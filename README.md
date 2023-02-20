# maptalks.mapsync

[maptalks](https://github.com/maptalks/maptalks.js) Map synchronization tool

## Install

### NPM

```sh
npm i maptalks
npm i maptalks.mapsync
# or
yarn add maptalks
yarn add maptalks.mapsync
```

### CDN

```html
<script src="https://unpkg.com/maptalks/dist/maptalks.js"></script>
<script src="https://unpkg.com/maptalks.mapsync/dist/maptalks.mapsync.js"></script>
```

## API

## MapSync

### constructor(maps)

```js
improt {
    MapSync
}
from 'maptalks.mapsync'

const mapSyncControl = new MapSync(maps);

// if you use cdn
const mapSyncControl = new maptalks.MapSync(maps);
```

### methods

* addMap(map)

```js
const map = new maptalks.Map(id, {
    center: [-0.113049, 51.498568],
    zoom: 14,
    baseLayer: new maptalks.TileLayer('base', {
        urlTemplate: 'https://{s}.basemaps.cartocdn.com/light_all/{z}/{x}/{y}.png',
        subdomains: ["a", "b", "c", "d"],
        attribution: '&copy; <a href="http://osm.org">OpenStreetMap</a> contributors, &copy; <a href="https://carto.com/">CARTO</a>'
    })
});
mapSyncControl.addMap(map);
```

* removeMap(map)

```js
mapSyncControl.removeMap(map);
```

* dispose()
