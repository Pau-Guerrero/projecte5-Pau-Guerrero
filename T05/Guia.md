
### 1. Configuració server
Quan s’obri la sessió, el primer que veurem serà una finestra amb el Server Manager.

![](img/image11.png)

Després canviarem el nom del servidor. Per fer-ho, anirem a Server Manager Properties dins del Server Manager, després a System Properties, clicarem a l’opció Change i posarem el nou nom. Quan acabem, ens demanarà reiniciar.

![](img/image12.png)

A continuació configurarem la xarxa. Anirem a Ajustos > Network & Internet i, on posa DNS server assignment, clicarem a Edit. Ho posarem en mode manual, activarem IPv4 i introduirem la IP 127.0.0.1.

![](img/image13.png)

Tornem al Server Manager, anirem a Manage i seleccionarem Add roles and features. S’obrirà una finestra i triarem Role-based or feature-based installation.

![](img/image14.png)

Després, a Server Selection, escollirem l’opció Select a server from the server pool.

![](img/image15.png)

Finalment, a Server Roles, activarem Active Directory Domain Services. Quan s’obri la finestra, marcarem també l’opció Include management tools.

![](img/image16.png)

Ara anirem a l’opció AD DS i clicarem Next.

![](img/image17.png)

Després, a Confirmation, li donarem a Instal·lar.

![](img/image18.png)

Quan torni el Server Manager, veurem una bandereta amb un triangle groc. Clicarem a l’opció Promote this server to a domain controller.

![](img/image19.png)

A Deployment Configuration, escollirem Add a new forest i posarem el domini translogicXX.test.

![](img/image20.png)

A Domain Controller Options, introduirem la contrasenya P@ssw0rd i activarem les opcions Domain Name System (DNS) server i Global Catalog (GC).

![](img/image51.png)

Finalment, a DNS Options, no tocarem res i clicarem Next.

![](img/image22.png)

A continuació, a Additional Options, veurem que se’ns posa un nom automàticament; li donarem a Next.

![](img/image52.png)

Després anirem a Review Options, on veurem un resum de les configuracions triades.

![](img/image25.png)

A la pantalla final començarem la instal·lació. Quan acabi, ens demanarà reiniciar.

![](img/image26.png)

Un cop reiniciat, quan tornem a entrar, veurem el nostre usuari amb el prefix davant del nom.

![](img/image53.png)

### 2.Configurar zona horaria
Per configurar la zona horària, anirem a Ajustos, després a Time & Language, i en l’opció de Zona horària seleccionarem UTC +1 Madrid.

![](img/image54.png)

### 3.DNS
Ara configurarem el DNS. Per fer-ho, anirem a l’opció DNS Manager:

![](img/image55.png)ç

Dins d’aquí anirem a Forwarders. Clicarem a Edit i afegirem el DNS de Google.

![](img/image56.png)