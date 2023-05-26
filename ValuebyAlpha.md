# Value by Alpha maps in QGIS

# Datenquelle: Geometrie und Attribute
[Bundestagswahl 2021](https://www.bundeswahlleiterin.de/bundestagswahlen/2021/ergebnisse/bund-99.html) 

Tabelle mit Wahlergebnisse bereinigen
![image](https://github.com/s91180/DTM/assets/134684032/0c170406-8bdf-4517-9250-7eba8c943ef0)

# QGIS
'''Vergleich SPD und CDU (Stimmenstärke der Partein darstellen)'''
OLAF
SPD>CDU

ARMIN
CDU<SPD

# Schritt 2
Symboleben auf Schwarz stellen
       
![image](https://github.com/s91180/DTM/assets/134684032/c1e3be4e-af85-4660-b380-6d6927f69767)

Regel für Ebene Alpha
Einfache Füllung unter Füllfarbe Daten definiertes Übersteuerung bearbeiten
![image](https://github.com/s91180/DTM/assets/134684032/c94b1e3a-df1c-4f1c-8126-fcf3f737cf9b)
![image](https://github.com/s91180/DTM/assets/134684032/76f4c3ee-b439-47a7-9513-940aa6877d49)

statt einen festen Alphawert wird dieser Werte passiert aus einem anderen Attributt 
        
set_color_part( 
'black',
'ALPHA',
  scale_linear( 
   "G" ,
   100000, 200000,
230,0)
   )
![image](https://github.com/s91180/DTM/assets/134684032/739fe7b7-4739-4f88-826a-d77c028b593c)

set_color_part( 
'white',
'ALPHA',
  scale_linear( 
   "G" /($area /100000),
  0, 1000,
230,0)
   )
        
![image](https://github.com/s91180/DTM/assets/134684032/44f89d90-5111-4657-9c93-70b74fd83c4f)
