Er zijn twee eenvoudige manieren om te achterhalen welk deel van het wandelnetwerk in de provincie Zuid-Holland al in OpenStreetMap staat.

## Overzicht met wandelnetwerken
OpenStreetMap contributor VMarc houdt [een overzicht](http://osma.vmarc.be/nl/networks/nl/rwn) bij van wandelroutenetwerken in Nederland en België in OpenStreetMap. 

## Query via Overpass Turbo

Je kunt de informatie over wandelnetwerken in Zuid-Holland opvragen met behulp van [Overpass Turbo](http://www.overpass-turbo.eu). Als je niet weet hoe Overpass Turbo werkt, kun je eerst [deze tutorial](https://github.com/FrieseWoudloper/workshop-maptime2016-overpass) volgen.

Met onderstaande query vraag je een lijst op van alle wandelnetwerken in OpenStreetMap binnen de provinciegrens van Zuid-Holland:

```
[out:csv(::"id", "name")];
area["name"="Zuid-Holland"]["admin_level"="4"];
relation["network" = "rwn"]["type" = "network"](area);
out;
```

Als je in de viewer van Overpass Turbo de geometrie wilt zien, voer dan deze query uit:

```
area["name"="Zuid-Holland"]["admin_level"="4"];
relation["network" = "rwn"]["type" = "network"](area);
out geom;
```

Je kunt ook alle gegevens opvragen (relations, ways en nodes). Dat duurt even. De query retourneert ongeveer 8 MB aan data.
```
area["name"="Zuid-Holland"]["admin_level"="4"];
relation["network" = "rwn"]["type" = "network"](area); 
>>;
out;
```

