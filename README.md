UA.js-Addons
============

URL-trackingcleaner


<script async src=”//storage.googleapis.com/outfox/urlCleaner_min.js”></script>

Registrera sedan UrlCleaner som en plugin till Google Analytics genom att anropa
ga(‘require’, ‘urlCleaner’). Efter att sidvisningen har skickats till Google Analytics anropas ga(‘urlCleaner:clean’) som tvättar URLen.

Kodexempel:

ga(‘create’, ‘UA-1234567-1′, ‘auto’);
ga(‘require’, ‘urlCleaner’);
ga(‘send’, ‘pageview’);
ga(‘urlCleaner:clean’);

 

Konfigurationsparametrar

Parameter	Typ	Beskrivning
debug	bool	Loggar info i konsolen om vilka parametrar som tagits bort av UrlCleaner om värdet sätts till true.
allowAnchor	bool	Tar bort parametrar även efter #-tecknet i URLen. Sätt denna till true om du skickar med kampanjparametrar efter #-tecknet.
params	string array	Om du vill att urlCleaner ska ta bort andra parametrar än de som används av Google Analytics skickas namnet på parametrarna i en array.
 

Kodexempel:

ga(‘require’, ‘urlCleaner’, {‘debug’: true, ‘allowAnchor’: true, ‘params’:['username','age']});
