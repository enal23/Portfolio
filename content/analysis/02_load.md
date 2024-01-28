Webbplatsers laddningstid
=======================

Uppgiften går ut på att testa och analysera webbplatsers laddningstid och utforska möjligheten till förbättring av laddningstiden.

Urval
-----------------------

Jag har valt dessa tre sidor att analysera:
### [Blocket](https://www.blocket.se/annonser/hela_sverige/fordon?cg=1000)
Jag valde blocket eftersom sidan har många bilder och är välbesökt.

### [Svenska Bostäder](https://www.svenskabostader.se/)
Svenska bostäder är min hyresvärd och valde dem för att jag inte kom på någon annan sida.

### [Bostadsförmedlingen i Stockholm](https://bostad.stockholm.se/)
En webbsida jag har besökt under många år och som har fått 3 lägenheter genom.

Metod
-----------------------

Resultaten fick jag genom att använda Google PageSpeed Insights och Chromes utvecklarverktyg 'Network'
På PageSpeed insights tog jag värdet 'Performance' och i 'Network' tog jag värdet som står vid 'Load:'

Resultat
-----------------------

Dokumentera dina resultat från din studie. Berätta vad du kom fram till, vilka resultat du hittade och observerade.

<iframe class="analysis-result" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vSvyDn-Xjo6q7eN9JPszHetmcJdcZGYmbjbIcDhH-fWiuVZ9OqBNSzpAC5zdbrnFt3QF4r6O4ePtvE7/pubhtml?gid=0&amp;single=true&amp;widget=true&amp;headers=false"></iframe>

Analys
-----------------------

### Blocket.se Fordonssök
![Blocket.se](../image/blocket.png?save-as=jpg&q=50&w=25%){.analysis-img}

Blocket fick sämst värde på alla mätkrav och hade störst resurs-storlek. Det beror på att de har många tredjeparts-skript.
Det som blocket gör bra är att deras bilder är i ett picture element med flera sources. Det gör så att olika bilder laddas beroende på användarens enhet.

### Svenska Bostäder 
![Svenska Bostäder](../image/svenskabostader.png?save-as=jpg&q=50&w=25%){.analysis-img}

Svenska Bostäder hade relativt bra betyg med snabbast laddningstid även om resurs-storleken var det dubbla jämfört med sidan med minsta antal filer. De har en stor bild på Stockholms stadshus som välkomnar en. Denna bild är satt som en bakgrundsbild med inline-css. Det hade varit bättre om de hade satt den i en picture med flera sources. Den är dock av filtypen jpg och rätt så liten(347kb). De har också många filer som hindrar rendering av sidan samt att de inte använder komprimering av text. 

## Bostadsförmedlingen
![Bostadsförmedlingen](../image/bostadsformedlingen.png?save-as=jpg&q=50&w=25%){.analysis-img}

Bostadsförmedlingen fick ungefär samma betyg som Svenska Bostäder på datorn men lika dåligt betyg som Blocket på mobilen. Den låga storleken filantalet var inte till hjälp. De har fått ett flertal varningar som överraskar. De har inte minifierat sin CSS eller aktiverat text-komprimering. Dessutom så flyttas layouten under laddningen. Deras bilder på framsidan är av filtypen png. 


Sammanfattad analys
-------------------
Det finns ett flertal genemsamma problem som måste lösas. Sidorna har många skript som laddas in, vilket i sin tur hindrar sidan från att ladda. En lösning på detta är att låta skripten laddas in sist eller att samla alla skript i ett. Detta är svårt om det är tredjeparts-skript som laddas in. Sidorna använder bra filtyp för bilder. Bilderna är beskärda så att för stora bilder inte laddas in. 

#### Vinnare
1. Bostadsförmedlingen
2. Svenska Bostäder
3. Blocket

#### Absolut Laddningstid
För att en webbsida ska kännas snabb så tycker jag inte att laddningstiden ska vara mer än 2s.
Om sidan tar längre tid än så får jag känslan av att det är en väldig tung sida som har mer information än jag behöver. Dessutom så känns det som