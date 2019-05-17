# Leaflet.GeographClickLayer

Creates a click event on Leaflet based maps that will show nearby Geograph Photos. 

* works with Geograph Britain, Ireland, Germany and Channel Islands - automatically!

https://www.geograph.org.uk/ , http://geo-en.hlipp.de/ , http://www.geograph.org.gg/

* Displays photos either by Subject location and/or Viewpoint location

* Nicely compliements https://github.com/barryhunter/Leaflet.GeographPhotos
   (which displays thumbnails ON the map) 

* and possibly https://github.com/barryhunter/Leaflet.GeographCoverage
   (which displays a grided coverage overlay)

* all three 'layers' can exist on same Leaflet map. for demo, see https://www.geograph.org.uk/mapper/combined.php ) 

* If want to use the 'Photo Subjects' and/or 'Photo Viewpoints' TileLayers, please  https://www.geograph.org.uk/contact.php


## Use

Include the Stylesheet, and Javascript (best added AFTER main Leaflet code)

        <link href="Leaflet.GeographClickLayer.css" rel="stylesheet" type="text/css" />
        <script src="Leaflet.GeographClickLayer.js"></script>

And requisites if dont have them already!

        <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.7.2/jquery.min.js"></script>
        <script src="https://s1.geograph.org.uk/mapper/geotools2.v7300.js"></script>


Then once have map, should be nothing more than 


        map.addLayer(L.geographClickLayer({apiKey:'enter-your-key-here'}));

On a mobile/touch device, can tweak the code slighty, so doesn't rely on mouse events. 

	map.addLayer(L.geographClickLayer({touch:true, domain: "https://m.geograph.org.uk", limit:6, apiKey:'enter-your-key-here'}));

Get a key at https://www.geograph.org.uk/admin/apikey.php


