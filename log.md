# 100 Days Of Code - Log

### R1D1: June 17, 2018 - Father's Day

**Today's Progress**: I added geoJSON coded location markers for flow stations along Sabino Creek and Tanque Verde to the OSM map I started at the Open Data Day.

**Thoughts** GeoJSON encoding is rather tedious, but it's nice to see the map getting populated. I'm not certain about the lat/long I used for the Bear Creek USFS station (I think it's on the wrong stream) and I'm a bit frustrated hard coding the geoJSON in the JS file, but I'll figure out how to tackle the XSS issues after I get all the pins in the right locations.

**Link(s) to work**
1. [Flow Monitor](https://github.com/CodeForTucson/flow-monitor)

### R1D2: June 18, 2018 - Monday

**Today's Progress**: I added geoJSON coded location markers for flow stations along the Tanque Verde and Rillito River to the OSM map I started at Open Data Day 2018.

**Thoughts** This is the day I gave my notice at WMG to accept a position as a contractor for the Microsoft Foundation. So, a bit of a momentous day. As far as my coding for today went, I am getting concerned that the Google Map (where the lat/lon for the markers was originally determined) is using a different reference system than OSM. The markers seem to be off a bit (sometimes quite a bit).

**Link(s) to work**
1. [Flow Monitor](https://github.com/CodeForTucson/flow-monitor)

### R1D3: June 19, 2018 - Tuesday

**Today's Progress**: I added geoJSON coded location markers for flow stations along the Santa Cruz River, Pantano Wash, Cienega Creek, and Rincon Creek to the OSM map I started at Open Data Day 2018.

**Thoughts** The manual geocoding is getting a bit tedious, but it's nearly done!

**Link(s) to work**
1. [Flow Monitor](https://github.com/CodeForTucson/flow-monitor)

### R1D4: June 20, 2018 - Wednesday

**Today's Progress**: Finished adding markers to the map.

**Thoughts** I have been coding the map using c9.io and had a problem today where the pins I added weren't being displayed. I tried restarting the server (multiple times), reloading the workspace, and checked for syntax errors more times than I like to admit. I even checked the Leaflet documentation to see if there was a limit to the number of pins that could be displayed. Turns out it was a c9 issue, because it worked when I loaded the code on my ubuntu machine and viewed the map. I guess I need to think about transitioning to AWS Cloud9, if I want to keep using c9. It seems pretty obvious they've stopped maintaining the legacy system.

**Link(s) to work**
1. [Flow Monitor](https://github.com/CodeForTucson/flow-monitor)

### R1D5: June 21, 2018 - Thursday

**Today's Progress**: I took a short break from the *Flow Monitor* app because I had an idea for another web app while I was working on it, so I took the time to document my thoughts while they were still fresh in my mind. I created a repo for the *Tucson Watershed Visualizer* and documented the roadmap in the wiki, as well as sketching some thoughts about how the pages might look in my design notebook.

**Thoughts** It was nice to take a short break from the somewhat tedious geoJSON coding (and styling that I need to work on next) to do a little design work on a new idea. But, tomorrow I need to get back to *Flow Monitor*.

**Link(s) to work**
1. [Tucson Watershed Visualizer](https://github.com/DainialPadraig/tucson-watershed-visualizer)

### R1D6: June 22, 2018 - Friday

**Today's Progress**: Moved the GeoJSON code into a separate file.

**Thoughts** This was not an especially satisfying change since now I've established an implicit dependency between the definition of the JavaScript variable monitorStations with its associated GeoJSON code and the stationmap.js file that uses the monitorStations variable located in the monitorstations.js file to display the markers on the map. Unfortunately, I haven't found a way to import a geoJSON file and assign it to a variable in stationmap.js without relying on a library like jQuery. I really don't want that additional overhead for such a simple app, but the alternative is embedding the GeoJSON in stationmap or having the implicit dependency - which is really bad software engineering. I'll need to think about this some more.

**Link(s) to work**
1. [Flow Monitor](https://github.com/CodeForTucson/flow-monitor)

