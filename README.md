# vue-lib-template

Base project to create a vue lib in npmjs with **rollup**, **eslint** and **storybook**.

## Installation

Install dependencies.

```bash
npm install
```

## Adjust values

- #### *package.json*
```json
{
  "name": "zenoft-ui-components",
  "description": "Package with all components used in zenoft applications",
  "author": "Zenoft",
  "main": "dist/zenoft-ui-components.ssr.js", 
  "module": "dist/zenoft-ui-components.esm.js",
  "browser": "dist/zenoft-ui-components.esm.js",
  "unpkg": "dist/zenoft-ui-components.min.js",
}
```
- **name**: unique name for use in npm (ex: npm i zenoft-ui-components)
- ***main, module, broswer, unpkg***: node_module file returned when import lib
  - **important**: change prefix to your package name  ex -> dist/{name}.{sufix}.js 

## Create and Update Components
#### ADD Component in your library

- Put your new component in directory *src/components/*;
- Once created it is necessary to **import** and **export** in ***src/components/index.js***;

#### Upload new version
- In ***package.json*** change the current version;
```json
{
  version: "1.1.2"
}
```

## Publish
- Publish the new version.
```bash
npm publish
```