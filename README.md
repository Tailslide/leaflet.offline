This branch is from a failed PR here: https://github.com/allartk/leaflet.offline/pull/72
I am keeping it around since it has functionality not in the main branch
(auto downloading of tiles, downsampling of missing tiles when offline)

Adds the following options:
 *   saveOnLoad: true - saves tiles to offline cache as they are loaded online
 *   downsample: true - if offline and tile missing for a given zoom level, downsample one from a lower zoom level 

I think this makes for a nicer offline experience.. the user never sees blank tiles, and everything they view online is later viewable offline.  Here is an example of what a downsampled tile looks like:

These can get turned on with these settings:


Downsampling looks like this:
![image](https://user-images.githubusercontent.com/5757188/122471718-d4527480-cf7c-11eb-92ca-6516f557308e.png)



# leaflet.offline version 2.x

Just a modern and slim library to store tiles offline.


Warning: The api of version 2 is different from version 1. 2 is ready (but tests are incomplete)

## Features in version 2

- Add geojson layer to show stored tiles on map 
- Split storage methods to seperate module. 
- Switch from localforage to idb and use Promises 

## Upgrading from version 1.x

Previously stored tiles will be lost!

## Dependencies

- [Leafletjs](http://leafletjs.com/)
- [idb](https://www.npmjs.com/package/idb) To store the tiles with promises

## Install

### Manual or Clone

Just use one of github's download methods (look under the releasestab ) and add dist/leaflet.offline.min.js in a script tag
to your page (after leaflet and localforage)

### With npm

The package and it's dependencies can also be downloaded into
your existing project with [npm](http://npmjs.com):

```
npm install leaflet.offline@next
```

In your script add:

```
import 'leaflet.offline'
```

### Development

For running the example locally, you'll need to clone the project and run:

```
npm install
npm start
```

Visit http://localhost:3000/ and watch the page reload when you change.

You can test your code with `npm test`. Please configure eslint in your editor if you wish to contribute.

**pull requests welcome**

## Api

Generate docs with

```
npm run-script docs
```
