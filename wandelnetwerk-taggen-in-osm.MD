*Hoe tag je een wandelnetwerk in OpenStreetMap?*    
Zet je schrap, want het is best ingewikkeld ;-)

OpenStreetMap kent drie verschillende gegevenstypen: nodes, ways en relations. Nodes zijn knopen; ways zijn lijnen of vlakken; relations zijn nodes, ways en/of relations die onderling een bepaald verband hebben.

Een wandelroutenetwerk bestaat uit knooppunten en routes die twee knooppunten met elkaar verbinden. Knooppunten zijn nodes en routes zijn relations. Een route bestaat uit één of meer wegdelen (ways).   

Een wandelroutenetwerk is zelf ook een relation, een samenhangend geheel van nodes en relations.

Een wandelroutenetwerk heeft minimaal de volgende tags:  
&nbsp;&nbsp;&nbsp;&nbsp;`name =` *naam van het wandelnetwerk*   
&nbsp;&nbsp;&nbsp;&nbsp;`network = rwn`   
&nbsp;&nbsp;&nbsp;&nbsp;`type = network`   

De route-relaties zijn lid van bovenstaande netwerk-relatie. Ze zijn als volgt getagt:     
&nbsp;&nbsp;&nbsp;&nbsp;`network = rwn`   
&nbsp;&nbsp;&nbsp;&nbsp;`type = route`   
&nbsp;&nbsp;&nbsp;&nbsp;`route = foot` of `route = hiking` of `route = walking`   
&nbsp;&nbsp;&nbsp;&nbsp;`note =` knooppuntnummer aan begin van de route-knooppuntnummer aan het eind van de route\*   
\* *Het laagste knooppuntnummer komt altijd vooraan en het hoogste achteraan.*   

Ways in een route-relatie hebben een vaste volgorde, van laag naar hoog knooppuntnummer!   

De knooppunten zijn ook lid van de netwerk-relatie. Zij hebben de volgende tag:   
&nbsp;&nbsp;&nbsp;&nbsp;`rwn_ref =` knooppuntnummer   

Zie ook http://osma.vmarc.be/nl/glossary en https://friesewoudloper.wordpress.com/2013/03/17/waddenwandelen-in-openstreetmap/. 

*Hoe kun je twee wandelnetwerken met elkaar verbinden in OpenStreetMap?*   
Dat doe je door de route-relatie die de netwerken verbindt, lid te maken van beide netwerk-relaties. Je geeft deze route-relatie een extra tag:   
&nbsp;&nbsp;&nbsp;&nbsp;`role = connection`   
Dit wordt niet door de JOSM-editor ondersteund en resulteert in waarschuwingen die je kunt negeren.   
Verder maak je de knooppunten aan beide kanten ook lid van beide netwerk-relaties.