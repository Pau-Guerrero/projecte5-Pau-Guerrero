# Guia T09
### Configuració de la màquina
En la màquina d’OpenVAS configurarem l’Adaptador 1 en mode NAT perquè tingui sortida a Internet i pugui actualitzar-se i descarregar tot el necessari, i afegirem un Adaptador 2 en mode Només amfitrió (Host‑Only).
![](img/2.png)
![](img/3.png)

En la màquina Metasploitable configurarem l’únic adaptador de xarxa en mode NAT.
![](img/34.png)

---
### Metasploitable
Per començar iniciarem la màquina Metasploitable des del nostre hypervisor i esperarem que arrenqui completament. Quan aparegui la pantalla de login, iniciarem sessió amb l’usuari msfadmin i la contrasenya msfadmin, que són les credencials predeterminades del sistema.
![](img/1.png)
---

### Instal.lació OpenVas
Al instal·lar OpenVAS ens demanarà quin usuari i contrasenya volem posar; li posarem com a usuari Admin i com a contrasenya també Admin.

![](img/4.png)

Després sortirà una finestra que diu “Upload subscription key now” i li donarem a Skip per continuar sense posar cap clau.

![](img/5.png)

Per últim apareixerà una finestra del selfcheck i simplement li donarem a Continue perquè faci les comprovacions automàtiques i acabi de preparar OpenVAS per poder començar a utilitzar-lo.

![](img/6.png)

### Configuració de OpenVas
Volem configurar les interfícies de xarxa, així que anirem al menú OS administration i li donarem a l’opció Setup.

![](img/7.png)

Un cop dins de Setup Menu, seleccionarem l’opció Network. Aquí és on trobarem totes les opcions relacionades amb la configuració de la xarxa.

![](img/8.png)

Dins del menú de Network, triarem l’opció Interfaces. Des d’aquest apartat podrem veure i editar les diferents targetes de xarxa de la màquina

![](img/9.png)

Ara configurarem els dos adaptadors de xarxa i en tots dos activarem el DHCP perquè agafin la IP automàticament; així no haurem de posar la IP a mà i només caldrà guardar els canvis perquè la configuració quedi aplicada correctament.

![](img/10.png)
![](img/11.png)
![](img/13.png)


### WEB
Ara mirarem la IP que té la màquina; obrirem el terminal i mostrarem la configuració de xarxa per saber quina adreça IP haurem de posar després al navegador per entrar a la web d’OpenVAS.
![](img/14.png)

Un cop sapiguem la IP, la posarem a la barra del navegador (per exemple http://IP) i se’ns obrirà la pàgina web d’OpenVAS, des d’on podrem fer tota la configuració i els escanejos.
![](img/15.png)

Quan entrem a la web, seleccionarem un dashboard i el deixarem tal qual ve per defecte, sense canviar res més, per poder continuar ràpidament amb la configuració.
![](img/16.png)

Ara afegirem un host nou i li posarem la IP de la màquina Metasploitable, ja que serà la màquina que volem escanejar, i a la descripció hi escriurem linux per identificar fàcilment el sistema.
![](img/17.png)

Ara crearem una targeta, li canviarem el nom a vulnerable Linux i en l’apartat de Hosts li posarem l’opció From hosts assets.
![](img/18.png)

Per poder continuar crearem una credencial de SSH; no tocarem cap altra opció, només li posarem un usuari i una contrasenya.
![](img/19.png)

Ara aquesta credencial de SSH la assignarem a la targeta que estàvem creant abans.
![](img/20.png)

Una vegada acabada la targeta, anirem a crear una tasca, li posarem un nom i li direm que escanegi la màquina que vulguem, en el meu cas la de vulnerable Linux.
![](img/21.png)

Ara li donarem a iniciar la tasca i esperarem que arribi al 100%, mirant la barra de progrés fins que acabi l’escaneig.
![](img/22.png)
![](img/23.png)

Un cop acabi la tasca veurem el resultat de l’escaneig i podrem revisar amb més detall tota la informació i les vulnerabilitats que ha trobat.
![](img/24.png)
![](img/25.png)

### RESULTATS
En aquest apartat veurem un resum general de l’escaneig, amb informació bàsica sobre la tasca, l’estat i una visió ràpida del que s’ha trobat.
![](img/26.png)

Aquí es mostren tots els resultats de l’escaneig, és a dir, les vulnerabilitats i avisos que OpenVAS ha detectat a la màquina.

![](img/27.png)

En aquest apartat apareixen els hosts que s’han escanejat, amb la seva IP i dades bàsiques de cada màquina analitzada.

![](img/28.png)

Aquí veurem els ports que s’han trobat oberts en els hosts escanejats, juntament amb el seu estat i el servei que hi està escoltant.

![](img/29.png)

En aquest apartat es mostren les aplicacions o serveis detectats als ports oberts, com ara servidors web, SSH o bases de dades.

![](img/30.png)

Aquí OpenVAS intenta identificar el sistema operatiu de cada host, mostrant si és Linux, Windows o un altre tipus de sistema.
![](img/31.png)

En aquest apartat es llisten les vulnerabilitats relacionades amb CVEs, amb els identificadors oficials perquè es puguin consultar més detalls.

![](img/32.png)

Aquí es mostren els certificats TLS detectats als serveis segurs, amb informació sobre la seva validesa i possibles problemes de seguretat.
![](img/33.png)
