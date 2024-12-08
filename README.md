# Calcul des éléments de la [suite de Syracuse](https://fr.wikipedia.org/wiki/Conjecture_de_Syracuse) en Drools.
<br>3 Règles sont nécessaires pour calculer la suite : 
<li>Une règle d'initialisation pour créer U0</li>
<li>Une règle pour calculer Un+1 lorsque Un est pair</li>
<li>Une règle pour calculer Un+1 lorsque Un est impair</li>
<br>Ces 2 dernières sont dans une table de décision.

Les temps de vol, temps de vol en altitude, et altitude max sont calculés par 3 autres règles.

Le webservice est exposé sur http://localhost:8080/syra :

curl -X 'POST' \
  'http://localhost:8080/syra' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
  "u0": 257}'