---
outline: deep
---

# LCircle

> Draw a path in the shape of a circle around a center positioned at `latLng` coordinates

## Demo

<script setup>
import L from "leaflet";
import "leaflet/dist/leaflet.css";
import { LMap, LTileLayer, LCircle } from '@vue-leaflet/vue-leaflet';
</script>

<LMap style="height: 350px" :zoom="8" :center="[47.21322, -1.559482]">
  <LTileLayer
    url="https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png"
    attribution="&amp;copy; <a href=&quot;https://www.openstreetmap.org/&quot;>OpenStreetMap</a> contributors"
    layer-type="base"
    name="OpenStreetMap"
  />
  <LCircle
    :lat-lng="[47.21322, -1.559482]"
    :radius="4500"
    :color="'red'"
  />
</LMap>

```vue{8-12}
<LMap style="height: 350px" :zoom="8" :center="[47.21322, -1.559482]">
  <LTileLayer
    url="https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png"
    attribution="&amp;copy; <a href=&quot;https://www.openstreetmap.org/&quot;>OpenStreetMap</a> contributors"
    layer-type="base"
    name="OpenStreetMap"
  />
  <LCircle
    :lat-lng="[47.21322, -1.559482]"
    :radius="4500"
    :color="'red'"
  />
</LMap>
```

## Props

| Prop name           | Description                                          | Type          | Values | Default       |
| ------------------- | ---------------------------------------------------- | ------------- | ------ | ------------- |
| pane                |                                                      | string        | -      | 'overlayPane' |
| attribution         |                                                      | string        | -      | null          |
| name                |                                                      | string        | -      | undefined     |
| layerType           |                                                      | string        | -      | undefined     |
| visible             |                                                      | boolean       | -      | true          |
| interactive         |                                                      | boolean       | -      | true          |
| bubblingMouseEvents |                                                      | boolean       | -      | true          |
| lStyle              |                                                      | object        | -      | null          |
| stroke              |                                                      | boolean       | -      | true          |
| color               |                                                      | string        | -      | '#3388ff'     |
| weight              |                                                      | number        | -      | 3             |
| opacity             |                                                      | number        | -      | 1.0           |
| lineCap             |                                                      | string        | -      | 'round'       |
| lineJoin            |                                                      | string        | -      | 'round'       |
| dashArray           |                                                      | string        | -      | null          |
| dashOffset          |                                                      | string        | -      | null          |
| fill                |                                                      | boolean       | -      | true          |
| fillColor           |                                                      | string        | -      | '#3388ff'     |
| fillOpacity         |                                                      | number        | -      | 0.2           |
| fillRule            |                                                      | string        | -      | 'evenodd'     |
| className           |                                                      | string        | -      | null          |
| radius              |                                                      | number        | -      | null          |
| options             | Leaflet options to pass to the component constructor | object        | -      | {}            |
| latLng              |                                                      | object\|array | -      | () => [0, 0]  |

## Events

| Event name     | Type    | Description                                        |
| -------------- | ------- | -------------------------------------------------- |
| update:visible | boolean | Triggers when the visible prop needs to be updated |
| ready          | object  | Triggers when the component is ready               |

## Slots

| Name    | Description | Bindings |
| ------- | ----------- | -------- |
| default |             |          |