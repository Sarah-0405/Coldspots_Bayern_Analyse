# Coldspots_Bayern_Analyse

Diese Repositorium enthält die Codes zur Analyse der Cold Spots in den bayerischen Städten mit>50.000 Einwohner*innen
Die Städte mit den Einwohnern über 50.000 wurden aus den Zensus-Daten entnommen. 


# Notebooks 
Die Städte-Polygone wurden über OSMnx bezogen, siehe Notebook "**01-Stadtgrenzen_osmnx.ipynb**". 

Anhand der Landoberlächentemperatur (LST) wurden die Cold Spots berechnet. Die LST wurde aus Landsat 8 Daten für den Zeitraum 2019-2024 bezogen, siehe Notebook "**02-LST_Dataframes_erstellen.ipynb**". Mittels Getis-Ord Gi* Algorithmus wurden die signifikant kälteren LST-Pixel einer Stadt identifiziert und als Cold Spot klassifiziert, siehe Notebook "**03-Coldspots_berechnen.ipynb**". 

Außerdem wurden Daten des Zensus 2022 für die drei Gruppen Menschen über 65 Jahre, Kinder unter 10 Jahre, und Menschen mit Migrationshintergrund bezogen und in ihrer räumlichen Verteilung analysiert, siehe Notebook "**04-Zensusdaten_zuschneiden_visualisieren.ipynb**". 

Schließlich wurde eine Erreichbarkeitsanalyse für die Cold Spots durchgeführt und diese Daten mit den Bevölkerungsdaten verknüpft, um die Erreichbarkeiten vulnerabler Gruppen zu Cold Spots im Vergleich zur Gesamtbevölkerung einzuordnen, siehe Notebook "**05-OSMnx_Erreichbarkeiten.ipynb**". 

Im Notebook "**06-LCZs_Cold_Spots_Kombination.ipynb**" wurden die Cold Spot Daten mit dem Local Climate Zones Datensatz verknüpft, um Muster in der räumlichen Verteilung der Cold Spots festzustellen.

Die Codes für die Plots sind im Notebook "**07-Plots.ipynb**" vorhanden. 


# Externe Daten 

Die für die Analyse benötigten Zensus-Tabellen im CSV-Format sind im Ordner "**_**" gespeichert, genauso wie die Rasterdatei der Local Climate Zones für Bayern ("**LCZs_bayern.tif**")
Alle weiteren Daten werden innerhalb der vorhandenen Codes erstellt und sind dadurch reproduzierbar. 






