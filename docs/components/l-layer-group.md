---
outline: deep
---

# LLayerGroup

> Group together elements of the maps including: markers, geoJSON, polylines and polygon, tooltip and popup.

::: warning
This still needs better documentation and examples.
:::

## Demo

<script setup>
import L from "leaflet";
import "leaflet/dist/leaflet.css";
import { LMap, LTileLayer, LLayerGroup, LMarker } from '@vue-leaflet/vue-leaflet';
</script>

<LMap style="height: 350px" :zoom="8" :center="[47.21322, -1.559482]">
  <LTileLayer
    url="https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png"
    attribution="&amp;copy; <a href=&quot;https://www.openstreetmap.org/&quot;>OpenStreetMap</a> contributors"
    layer-type="base"
    name="OpenStreetMap"
  />
  <LLayerGroup>
    <LMarker :lat-lng="[47.21322, -1.559482]" />
  </LLayerGroup>
</LMap>

```vue
<LMap style="height: 350px" :zoom="8" :center="[47.21322, -1.559482]">
  <LTileLayer
    url="https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png"
    attribution="&amp;copy; <a href=&quot;https://www.openstreetmap.org/&quot;>OpenStreetMap</a> contributors"
    layer-type="base"
    name="OpenStreetMap"
  />
  <LLayerGroup>
    <LMarker :lat-lng="[47.21322, -1.559482]" />
  </LLayerGroup>
</LMap>
```

## Props

| Prop name   | Description                                          | Type    | Values | Default       |
| ----------- | ---------------------------------------------------- | ------- | ------ | ------------- |
| pane        |                                                      | string  | -      | 'overlayPane' |
| attribution |                                                      | string  | -      | null          |
| name        |                                                      | string  | -      | undefined     |
| layerType   |                                                      | string  | -      | undefined     |
| visible     |                                                      | boolean | -      | true          |
| options     | Leaflet options to pass to the component constructor | object  | -      | {}            |

## Events

| Event name     | Type    | Description                                        |
| -------------- | ------- | -------------------------------------------------- |
| update:visible | boolean | Triggers when the visible prop needs to be updated |
| ready          | object  | Triggers when the component is ready               |

## Slots

| Name    | Description | Bindings |
| ------- | ----------- | -------- |
| default |             |          |