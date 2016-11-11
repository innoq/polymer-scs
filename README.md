# \<scs\>



## Install the Polymer-CLI

First, make sure you have the [Polymer CLI](https://www.npmjs.com/package/polymer-cli) installed. Then run `polymer serve` to serve your application locally.

## Viewing Your Application

```
$ polymer serve
```

## Building Your Application

```
$ polymer build
```

This will create a `build/` folder with `bundled/` and `unbundled/` sub-folders
containing a bundled (Vulcanized) and unbundled builds, both run through HTML,
CSS, and JS optimizers.

You can serve the built versions by giving `polymer serve` a folder to serve
from:

```
$ polymer serve build/bundled
```

## Running Tests

```
$ polymer test
```

Your application is already set up to be tested via [web-component-tester](https://github.com/Polymer/web-component-tester). Run `polymer test` to run your application's test suite locally.

# \<scs\> as Container

Usage:

* cd to 'docker' folder
* type 'make run'
* browse to http://localhost/

5 images are created/used:

* scs-cors-nginx: nginx image based on nginx:alpine and with enabled-by-default CORS
* scs-assets: Asset server with the required Polymer components
* scs-sys1/2/3: Simulated systems 1,2 and 3
* scs-dashboard: Simple entry system

Since there is no DNS, systems are separated by ports

* 89 -> asset server
* 80 -> Dashboard
* 81 -> System 1
* 82 -> System 2
* 83 -> System 3
