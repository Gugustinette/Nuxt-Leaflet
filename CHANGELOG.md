# Changelog

## v1.0.13

This release drops the old `leaflet-runtime.ts` to take advantage of the [Vue Leaflet behavior](https://github.com/vue-leaflet/vue-leaflet/blob/db34dff79cc62bc6fa51357e953e9bcf55725c94/src/components/LMap.vue#L250-L256) when importing Leaflet.
This prevent Leaflet from being imported literally everywhere in the app, even if it isn't used.

### 🏡 Chore

- **Drop Leaflet runtime import:** [#1](https://github.com/Gugustinette/Nuxt-Leaflet/issues/1)

### ❤️  Contributors

- Gugustinette <mercier.augustin@outlook.fr>
- Daniel Roe <daniel@roe.dev>

## v1.0.12

Initial Release

### 🏡 Chore

  - **Auto-import Vue Leaflet components:** [v1.0.1](https://github.com/Gugustinette/Nuxt-Leaflet/commit/ae50d3ef634b4903878f3c2b81b0ba7a71795707#diff-9b09a2431586002325ecf88d666c07eedba4dbdec83acfa5890526aa2e18764c)
  - **Auto-import Leaflet as L:** [v1.0.3](https://github.com/Gugustinette/Nuxt-Leaflet/commit/67f25f8c8cf59e1c89711e7a938dd292d4e358df#diff-082d2c8211be1dd40cb6dc5a124074d5bb825b41568250ce265dfa4d3e0c601a)

### ❤️  Contributors

- Gugustinette <mercier.augustin@outlook.fr>
