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

### R1D7: June 23, 2018 - Saturday

**Today's Progress**: Started setting up a Raspberry Pi 3 official touchscreen for the Living Lab and Learning Center weather monitor project. Created a github library, installed and tested libraries on the Raspberry Pi, and started looking into the Kivy framework to decide if that's an approach I want to take for the weather displays on the touchscreen or not. Kivy does have 10 point touchscreen compatible graphics capabilities and is the framework used by the Raspberry Pi Foundation for the weather stations they distributed to schools. I just need to decide if learning a new framework and display language is really worth the time or if I can get the functionality I want out of the Mesonet API by itself. It will require more experimenting.

**Thoughts** I'm at a temporary impasse on the *Flow Monitor* app right now. I'm trying to decide what I want to implement next on it, so I took some time to work on the weather data montior for the Living Lab. It's a project I have a soft deadline for, so I'd like to make some progress on it. Today was mostly research and setting up the development environment and a repo, but I think I can make some progress on it tomorrow after doing some comparative experiments with [Kivy](https://kivy.org/#home) and the [Mesonet API](https://synopticlabs.org/api/mesonet/).

**Link(s) to work**
1. [LLLC Weather Monitor](https://github.com/DainialPadraig/lllc-weather)

### R1D8: June 24, 2018 - Sunday

**Today's Progress**: Decided to give Kivy a try for the data visualization, so spent quite a bit of time installing it on the Raspberry Pi (pip is really slow, even on the Pi3). Also installed MesoPy to access the MesoWest weather data through Python and wrote a really short test script to download some precip data. Read through some documentation for both.

**Thoughts** Really don't have anything working. Going to have to check the path for MesoPy because the Python script's not finding it. Haven't tried building a "hello world" for Kivy yet. That will be tomorrow.

**Link(s) to work**
1. [LLLC Weather Monitor](https://github.com/DainialPadraig/lllc-weather)

### R1D9: June 25, 2018 - Monday

**Today's Progress**: Experimented with data retrieval from MesoWest using MesoPy.

**Thoughts** Got MesoPy working. Retrieved current weather station data and precip for the year data. Results looked good. My Python is rusty, thinking I might want to brush up on it. Might also make sense to evaluate some Python tutorials/books to see what would be good to recommend to some of the students and teachers I will be working with. There's certainly A LOT out of material out there.

**Link(s) to work**
1. [LLLC Weather Monitor](https://github.com/DainialPadraig/lllc-weather)

### R1D10: June 26, 2018 - Tuesday

**Today's Progress**: Continued experimenting with MesoWest data retrieval using MesoPy. Also tried to format my code to conform to the [Google Python Style Guide](https://github.com/google/styleguide/blob/gh-pages/pyguide.md#s3.17-main) and running Pylint on my code. Created separate functions for displaying different datasets.

**Thoughts** My Python's sloppy, but I was happy that I got up to 4.21/10 on pylint. Got more work to do to write good Python code, to be sure. Also need to start parsing the data I really want to display. I'm just dumping dicts to the screen right now.

**Link(s) to work**
1. [LLLC Weather Monitor](https://github.com/DainialPadraig/lllc-weather)

### R1D11: June 27, 2018 - Wednesday

**Today's Progress**: Continued experimenting with MesoWest data retrieval using MesoPy. Created separate functions for displaying all the expected displays.

**Thoughts** Spent most of my time today researching Python and MesoWest libraries - not really doing much coding except in the Python shell to see if the libraries were working the way I expected them to work.

**Link(s) to work**
1. [LLLC Weather Monitor](https://github.com/DainialPadraig/lllc-weather)

### R1D12: June 30, 2018 - Saturday

**Today's Progress**: Retrieved and displayed the current weather values I wanted from the API and the precip for this month and the previous year at the same time, as well as the precip for the year-to-date. This is the data portion of the visualization I want to do on the monitor.

**Thoughts** Missed two days in the challenge due to leaving my old job (had a double shift trying to get everything cleaned up, documented, and handed over). Really not happy about that, but I think I made some good progress today extracting the variables I want to display from the dictionary of weather station data returned by the API.

**Link(s) to work**
1. [LLLC Weather Monitor](https://github.com/DainialPadraig/lllc-weather)

### R1D13: July 1, 2018 - Sunday

**Today's Progress**: Retrieved and displayed the temperature stats for the month and year.

**Thoughts** I need to start thinking about the data visualization now. I've figured out how to retrieve the variables I need from MesoPy (or at least most of them) - now I need to working on visualizations. Need to work some Kivy examples starting tomorrow, to get familiar with the framework.

**Link(s) to work**
1. [LLLC Weather Monitor](https://github.com/DainialPadraig/lllc-weather)

### R1D14: July 2, 2018 - Monday

**Today's Progress**: Added previous month's rainfall to the monthly rainfall data display and started investigating NOAA climate API access in Python.

**Thoughts** I realized I still need to do some more backend data work before moving on to the graphical visualization. Getting data from previous years was pretty straight forward in MesoPy - except for one inconsistent behavior: when querying two station ids in the same request, the lists in the returned dictionary were not in a consistent order (the first id should be list 0 and the second should be list 1, but sometimes they are backwards). To make sure I knew what was going to be returned, I made separate calls for each station. 

Next, I wanted to retrieve historical climate data (like average rainfall for a given month in Tucson). This turned out to be harder to find. NOAA is the keeper of US climatological data, but much of it is no longer being updated or made freely available. (Big surprise given the current administration's hostility toward climate data, right?) After searching through the site documentation, I think I finally found a PyPi library that will get the data I need. I'll have to experiment with that tomorrow.

**Link(s) to work**
1. [LLLC Weather Monitor](https://github.com/DainialPadraig/lllc-weather)

### R1D15: July 3, 2018 - Tuesday

**Today's Progress**: Reading through documentation about NOAA Climate Data Online Web Access and experimenting with various Python packages to access the data. IOW, not much progress today.

**Thoughts** Accessing the NOAA CDO web data is not as straight forward as I had hoped and the Python packages I had hoped might work from PyPi didn't work with Python 2.7 - even though they claimed they did. It's going to take a bit more tinkering to get the NOAA web portal to accept my access token and return some usable data.

**Link(s) to work**
1. [LLLC Weather Monitor](https://github.com/DainialPadraig/lllc-weather)

### R1D16: July 4, 2018 - Independence Day

**Today's Progress**: Experimenting with curl calls to NOAA CDO. Getting inconsistent results, but did get some metadata back.

**Thoughts** The NOAA CDO web access is not as well documented or intuitive as one would hope. I was able to make curl calls from the linux command line to retrieve metadata using the CDO token I was issued, but getting the desired data back is pretty hit or miss. I did get some real-time data back for precip, but can't seem to retrieve the climatic normals data I'm trying to get. Going to take a bit more experimenting and then I'll need to implement the curl request as a web query in Python. Most likely using urllib2.

**Link(s) to work**
1. [LLLC Weather Monitor](https://github.com/DainialPadraig/lllc-weather)

### R1D17: July 5, 2018 - Thursday

**Today's Progress**: Still playing with NOAA data without much success.

**Thoughts** Couldn't seem to retrieve the desired normals data from CDO, so I looked at some other sources. There are text files of [NOAA 1981-2010 Climate Normals](https://www1.ncdc.noaa.gov/pub/data/normals/1981-2010/readme.txt) that can be accessed via FTP or HTTP. Tried to get the precip file using urllib2 and parse it. I know the data is in the file, having viewed it, but getting 404 errors when accessing it through Python. Perhaps the smarter thing to do would just be to create some lists of the normal data, since it only changes once a decade!

**Link(s) to work**
1. [LLLC Weather Monitor](https://github.com/DainialPadraig/lllc-weather)

### R1D18: July 6, 2018 - Friday

**Today's Progress**: Finally was able to get normal data from the NOAA climate normals website. Also restructured my repo to follow the suggestions in _The Hitchhiker's Guide to Python_.

**Thoughts** Making some progress on getting data from NOAA. It's still a pain, since it's text, but I can parse that and build the lists that I want for displaying monthly normals. Also really enjoying reading _The Hitchhiker's Guide to Python_, there are some great tips about style and usage for Python in there.

**Link(s) to work**
1. [LLLC Weather Monitor](https://github.com/DainialPadraig/lllc-weather)

### R1D19: July 9, 2018 - Monday

**Today's Progress**: Worked some unit test examples from _The Hitchhiker's Guide to Python_.

**Thoughts** Missed two days of coding due to preparing for a meeting and starting my new job. Disappointing, but getting back in the saddle!

**Link(s) to work**
1. [LLLC Weather Monitor](https://github.com/DainialPadraig/lllc-weather)
