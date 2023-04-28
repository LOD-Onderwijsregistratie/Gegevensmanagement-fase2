
# Het installeren van het script Identitynote in Archi

De jArchi plugin is een extensie van javascript bij Archi om scripts te runnen. Deze scripts hebben toegang tot de archimate modellen en kunnen die manipuleren. De verzameling scripts vormt een geschikte toolset voor gebruik door ‘architectuurbeheer’.   Uitleg van jArchi is hier te vinden: https://github.com/archimatetool/archi-scripting-plugin/wiki

De plugin wordt geleverd met voorbeeld-scripts.  Andere plekken om scripts te vinden:

* https://github.com/archi-contribs/jarchi-community-script-pack
* https://gist.github.com/search?utf8=%E2%9C%93&q=%23jarchi+extension%3Aajs&ref=searchresults
* https://github.com/nasjonal-arkitektur/kode-archiscripts
* https://gitlab.com/vng-realisatie/architectuur/tools/archi-scripts (na autorisatie).

Ook is er aan actieve community met veel experts die hulp kunnen bieden: https://forum.archimatetool.com

jArchi is in tegenstelling tot (co)Archi geen freeware, ook al kost het geen drol. Het is beschikbaar voor iedereen die maandelijks 3 euro bijdraagt via Patreon.  

1.	Bemachtig de jArchi-script plugin via Patreon: https://www.patreon.com/architool/posts?filters[tag]=jArchi en plaats deze in de plugin folder van Archi (doorgaans: C:\Program Files\Archi\plugins).

2.	Ga in Archi naar het menu Help/Manage Plug-ins en activeer de plugin. Archi herstart vanzelf. 

3.	De eerste keer dat jArchi is geïnstalleerd moeten de “Scripts Manager” en de “Scripts Console”  zichtbaar worden gemaakt. Doe dit met de “Reset Window Layout” van het “Window” menu.  Op “Scripts Manager” klik op de "Restore Example Scripts" button. De voorbeeld jArchi worden in de "examples" folder gezet.

4.	Kopieer het volgende script:
https://github.com/onderwijsarchitectuur/Gegevensmanagement/blob/master/scripts/Add%20identynote%20on%20view.ajs
naar een gebruikersfolder (voorstel C:\Users\....\Documents\Archi\scripts)

5.	Het identitynote script kan worden afgespeeld in de “Scripts Manager” als er een view is geselecteerd.
