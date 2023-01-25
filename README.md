
# Gegevensmanagement
Deze github-repository bevat het kernmodel van business, toepassing en technische architectuur van het domein gegevensmanagement. Deze (tijdelijke) repository is ingericht om te werken met (co)Archi.

## (co)Archi
Archi is een populaire open source tool voor he maken van architectuurmodellen. Die hier te vinden: [Archi download-pagina](https://www.archimatetool.com/download/). Het is freeware maar een donatie wordt gewaardeerd en sommige dingen zijn alleen beschikbaar  voor donors (voor een verwaarloosbaar bedrag). Uitgangspunt van deze beschrijving is dat de werking van Archi bekend is, het is in elk geval intuïtief.
Archi kan “git-friendly’ gemaakt met een extra plugin genaamd coArchi. Dit is ook open source en de code en wiki van coArchi vind je hier: [coArchi github](https://github.com/archimatetool/archi-modelrepository-plugin). Op de wiki van coArchi vind je setup- en configuratie aanwijzingen.  In het kort. 
1.	Download the coArchi plug-in zip file from the [coArchi plugins page](https://www.archimatetool.com/plugins/) 
2.	In Archi, select "Manage Plug-ins..." from the main Help menu. From the Plug-ins Manager window, select "Install New..." and select the plug-in file and then, when prompted, allow Archi to restart
3.	The "Collaboration" menu should now be visible
4.	Configure coArchi through Archi’s menu Edit/Preferences/Collaboration. At least:
     * Naam en email
     * Lokale workspace (default)
     * Primary password (wordt gevraagd als je Archi opnieuw opstarten en wil klonen of mergen).
 
 

## Beveiliging Github-Archi. 
Maak in Github een Personal Access Token (PAT) aan bij je persoonlijke account. Volg linker menu:  Settings/Developer setting/Personal Access Token.

Alternatief: maak met Git-bash een SSH-sleutelpaar en voer de  publieke sleutel in bij je persoonlijke account via het linker menu Settings/SSH-keys. 

## Gitflow


### Klonen in coArchi

Ga in  het  collaboration-menu naar de optie: Import Remote Model to Workspace.  Er volgt een popup:
![coarchi-control](https://github.com/onderwijsarchitectuur/Gegevensmanagement/images/Afbeelding4.svg)

Hier vul je in (https-variant):
1. URL: Dit is het internetadres van de repo. Dat vind je achter de groene "code" button in Github. Kies de https-versie.
2. Username: Dit mag een random naam zijn, maar niet afwezig
3. Password: Hier vul je je Personal Access Token (PAT) van Github in. 

Of vul je in (ssh-variant):
1. URL: Dit is het internetadres van de repo. Dat vind je achter de groene "code" button in Github. Kies de SSH-versie.
2. Username: Dit mag een random naam zijn, maar niet afwezig
3. Password: blijft leeg. 

 

### Lokaal wijzigen in Archi
Nu is het mogelijk om lokaal wijzigingen door te voeren in het model.  De meest eenvoudige gitflow is dit:

![gitflow-simpel](https://github.com/onderwijsarchitectuur/Gegevensmanagement/images/blob/master/Afbeelding1.png)
Er is één branche, de master of mainline. Meerdere architecten kunnen tegelijk werken aan hetzelfde model in hun eigen (archi-)omgeving.   Sla het op in lokale workspace (control-s) en doe een commit in het Collaboration-menu om de wijzigingen te bevestigen 
 

### Publiceren
Daarna kun je de gewijzigde model in het Collaboration menu van coArchi centraal maken met de optie Publish:
Archi controleert op mergeconflicten per architectuurelement. Als die er zijn Archi beide varianten en kan de architect kiezen om de centrale versie te overrulen met zijn eigen versie of om zijn eigen versie te af te blazen.

![Merge-conflict](https://github.com/onderwijsarchitectuur/Gegevensmanagement/images/blob/master/Afbeelding2.png) 

### Beschermde master/mainline
Bovenstaande gitflow is eenvoudig maar wordt bij een groter aantal architecten al snel onoverzichtelijk. Iedereen kan direct dingen in de master publiceren.  De volgende stap is dat de master alleen kan worden aangepast na een formeel besluit. Hiertoe kunnen de architecten in Archi extra branches introducerenn.

![coarchi-control](https://github.com/onderwijsarchitectuur/Gegevensmanagement/images/blob/master/Afbeelding3.png)
 
Stappen:
1.	Stel, in de Git-repository zit een model met één branch, de Master. Deze repository is gekloond in (co)Archi, collaboration-menu : Import Remote Model to Workspace.

2.	Dit model heeft in de ‘branches view’ van coArchi initieel maar één branche, tevens ‘current’. Dat verandert nu. Rechtermuisklik op deze branche geeft deze optie ”Add New Branche to Current Branche”. Deze geef je een herkenbare naam zodat andere architecten weten wie aan het werk is en met wat, “Bedrijfsobjecten_2023” bijvoorbeeld. Klik op “add&checkout  zodat deze extra branche als ‘current’ is opgenomen in (co)Archi. 

3.	Aansluitend kun je op de gebruikelijke wijze in Archi wijzigingen aanbrengen in deze werkomgeving en deze saven/committen. Het  model is nu nog lokaal. Dat kun je zo laten als een soort zandbak. 

4.	Na “Publish” verschijnt deze branche/werkomgeving ook in de git-repository. Het is daarmee centraal veilig gesteld. En als andere collaborators willen, kunnen ze (na een “Refresh” ) deze werkomgeving bekijken en eventueel bewerken.

5.	De master is afgesloten voor individuele wijziging. Het geven van toestemming is een groepsproces.

6.	De branche/werlomgivng is nog niet gemerged in de Master. Dat gebeurt met een zogenaamde Pull Request in de git-repository. 

Om merge-conflicten te voorkomen wordt het aangeraden om de delta’s  in de werkomgevingen klein te houden en om dagelijks een refresh te doen in het Collaboration model van Archi.
