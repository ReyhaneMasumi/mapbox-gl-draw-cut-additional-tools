[![NPM](https://img.shields.io/npm/v/mapbox-gl-draw-additional-tools.svg)](https://www.npmjs.com/package/mapbox-gl-draw-additional-tools)
![Develop](https://github.com/reyhanemasumi/mapbox-gl-draw-additional-tools/workflows/Develop/badge.svg)
![Release](https://github.com/reyhanemasumi/mapbox-gl-draw-additional-tools/workflows/Release/badge.svg)

# mapbox-gl-draw-additional-tools

A custom mode for [MapboxGL-Draw](https://github.com/mapbox/mapbox-gl-draw) to cut polygons

## [DEMO](https://reyhanemasumi.github.io/mapbox-gl-draw-additional-tools/)

![A Gif showing demo usage](demo/public/demo.gif)

## Install

```bash
npm install mapbox-gl-draw-additional-tools
```

or use CDN:

```html
<script src="https://unpkg.com/mapbox-gl-draw-additional-tools"></script>
```

## Usage

```js
import mapboxGl from 'mapbox-gl';
import MapboxDraw from '@mapbox/mapbox-gl-draw';
import AdditionalTools from 'mapbox-gl-draw-additional-tools';

const map = new mapboxgl.Map({
    container: 'map', // container id
    style: 'mapbox://styles/mapbox/streets-v11',
    center: [-91.874, 42.76], // starting position
    zoom: 12, // starting zoom
});

const draw = new MapboxDraw({
    modes: {
        ...MapboxDraw.modes,
    },
    userProperties: true,
});
map.addControl(draw);
map.addControl(AdditionalTools(draw), 'top-right');
```

## [Example](https://github.com/ReyhaneMasumi/mapbox-gl-draw-additional-tools/blob/main/demo/src/App.js)

## License

MIT © [ReyhaneMasumi](LICENSE)
