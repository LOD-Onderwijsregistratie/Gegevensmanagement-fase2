
# Gegevensmanagement
Deze git-repository bevat het kernmodel van business, applicatie en technische architectuur van het domein gegevensmanagement. Deze (tijdelijke) repository is ingericht om te werken met (co)Archi. Uitgangspunt is dat (co)Archi is geïnstalleerd.

## Maak een token in Git 
Maak in Git een Personal Access Token (PAT) aan bij je persoonlijke account.
* Github:  Volg linker menu:  Settings/Developer setting/Personal Access Token.

Alternatief: maak met Git-bash een SSH-sleutelpaar en voer de  publieke sleutel in bij je persoonlijke account 
* Github: via het linker menu Settings/SSH-keys. 


## Maak coArchi de client

Ga in  het  collaboration-menu naar de optie: Import Remote Model to Workspace.  Er volgt een popup:

Hier vul je in (https-variant):
1. URL: Dit is het internetadres van de repo. Dat vind je achter de groene "code" button in Github. Kies de https-versie.
2. Username: Dit mag een random naam zijn, maar niet afwezig
3. Password: Hier vul je je Personal Access Token (PAT) van Git in. 

Daarnaast is de SSH variant
- inrichten: 
1. Ga naar het menu Edit/Preferences/Collaboration
2. Vind de identity file, de private key.
3. Voer het identity wachtwoord in dat je hebt opgegeven bij het maken van de SSH keys.

- uitvoeren:
1. URL: Dit is het internetadres van de repo. Dat vind je achter de groene "code" button in Github. Kies de SSH-versie.
2. Username: Dit mag een random naam zijn, maar niet afwezig
3. Password: blijft leeg. 
