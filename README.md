# \<search-location-project\>

Polymer application that allows a user to search for a location and other special things :)

# My Thought Process

The big thing that is stressed with Polymer is the notion of 'reusable
components.' I took advantage of this by using the existing google-map,
google-map-marker, geo-location, and some of the Polymer paper components.
Instead of writing my own functions to make requests with the
Google API's, all I needed to do was bower install the polymer components that I
wanted to use and... voila! The components, that are maintained by Google and
other developers, were available at my disposal.

The SpaceCam app will let the user search for any location that they search and
display the location(s) on the map. The names of the locations will also be
listed in the "List of Locations" section. Users can select the name and
see where the location is located on the map - communication between the list
and the map with markers! The user can also click on the marker that gets
centered on the map and some information is listed there for the user to see,
like the address, the rating, an icon specifying what kind of location it is,
and whether or not the location is open.

There were a few limitations with using the Polymer components that I did. While
it was nice to save some time to get rolling with using the APIs, the reusable
components had some bugs - I had to open a few issues on Github to get them
looked at. For example, the map's "fit-to-markers" function did not work, and it
was difficult to access the 'google-map-markers' when they were already added to
the 'google-map'.

I also added a few tests to this suite. Polymer uses web-component-tester to
test the project. The tests that I included were testing that the geo-location
element returns the correct current location and loads a list of empty results
and expects a certain response. 

*** Side Note: I usually put CSS stylings in an external page, but the thing
with Polymer is that it uses Shadow DOM styling rules, so the styling must be
contained in a style tag inside the element's local DOM ***

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

This will create builds of your application in the `build/` directory, optimized to be served in production. You can then serve the built versions by giving `polymer serve` a folder to serve from:

```
$ polymer serve build/default
```

## Running Tests

```
$ polymer test
```

Your application is already set up to be tested via [web-component-tester](https://github.com/Polymer/web-component-tester). Run `polymer test` to run your application's test suite locally.
