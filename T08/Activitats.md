# ACTIVITATS T08
Podem comprovar el funcionament d'antimalware fent servir programari específic o amb fitxers amb malware real (no recomanat).

1. Seguiu les instruccions de l'enllaç que trobareu a https://www.eicar.org per a obtenir una còpia del test EICAR.

2. Pot ser que hagueu de desactivar de forma temporal el detector del navegador web i el de Windows per a poder baixar-lo. Expliqueu com es fa.
Activeu i comproveu si el detecta l'antimalware escollit.
Torneu a desactivar la detecció en temps real. Proveu ara a tornar a baixar i a amagar el virus EICAR dintre un arxiu comprimit en formats diferents. Podeu fer servir eines com winzip, winrar o 7zip per comprimir el fitxer. Torna a activar l'antimalware. Indica en cada cas si l'antimalware detecta l'amenaça:

 zip
 tar
 7zip


### Sistemes protecció Windows 11
1. Quines proteccions incorporar Windows 11 a la seccció de "Protección antivirus y contra amenazas"?

2. Quines opcions tenim a "Control de aplicaciones y navegador"?

3. Investigueu quines opcions específiques hi ha per la protecció contra ransomware a Windows 11.

### Prova pràctica de protecció contra Ransomware
Ara comprovarem el funcionacionament específic de les proteccions contra ransomware, feu el següent:

1. Afegiu dins la carpeta "Documents" uns quants arxius TXT.

2. Desactiveu, si està activada prèviament, la protecció contra ransomware.

3. Descarregeu el fitxer de prova de ransomware de https://github.com/JoelGMSec/PSRansom. Es tracta d'un script de PowerShell que simula el comportament d'un ransomware. Com per defecte, Windows 11 restringeix l'execució d'scripts de PowerShell, haureu de canviar la política d'execució per permetre-ho, obrint una finestra de PowerShell com a administrador i executant la següent ordre:

Set-ExecutionPolicy -ExecutionPolicy unrestricted


4. Obre una consola de PoweShell a la carpeta on hagis descarregat l'script i executa'l amb la següent ordre:

.\PSRansom.ps1 -e C:\Users\%USERNAME%\Documents -s 127.0.0.1 -p 80 -x

