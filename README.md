# Coldspots_Bayern_Analyse
Diese Repositorium enthält die Codes zur Analyse der Cold Spots in den bayerischen Städten mit >50.000 Einwohner*innen
Die Städte mit den Einwohnern über 50.000 wurden aus den Zensus-Daten entnommen. 

Die Städte-Polygone wurden über OSMnx bezogen, siehe Notebook "Polygone_Städte_über_50tsd.ipynb". 
Anhand der Landoberlächentemperatur (LST) wurden die Cold Spots berechnet. Die LST wurde aus Landsat 8 Daten für den Zeitraum 2019-2024 bezogen, siehe Notebook "LST_Dataframes_2019_2024_erstellen.ipynb". Mittels Getis-Ord Gi* Algorithmus wurden die signifikant kälteren LST-Pixel einer Stadt identifiziert und als Cold Spot klassifiziert, siehe Notebook "2019_2024_KNN_Gi_Puffer.ipynb". 

Im Notebook "LCZs_Cold_Spots_Kombination.ipynb" wurden die Cold Spot Daten mit dem Local Climate Zones Datensatz verknüpft, um Muster in der räumlichen Verteilung der Cold Spots festzustellen.

Außerdem wurden Daten des Zensus 2022 für die drei Gruppen Menschen über 65 Jahre, Kinder unter 10 Jahre, und Menschen mit Migrationshintergrund bezogen und in ihrer räumlichen Verteilung analysiert, siehe Notebook "Zensusdaten_zuschneiden_visualisieren.ipynb". 

Schließlich wurde eine Erreichbarkeitsanalyse für die Cold Spots durchgeführt und diese Daten mit den Bevölkerungsdaten verknüpft, um die Erreichbarkeiten vulnerabler Gruppen zu Cold Spots im Vergleich zur Gesamtbevölkerung einzuordnen, siehe Notebook "OSMnx_Erreichbarkeiten_.ipynb". 
