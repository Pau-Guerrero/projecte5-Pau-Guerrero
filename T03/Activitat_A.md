
# GUIA T03
---

### 1) Configuració dels adaptadors de xarxa
Primer configurarem la xarxa de la màquina virtual. Posarem el **primer adaptador** en mode **NAT** per donar accés a Internet, i el **segon adaptador** en mode **Només Anfitrió** per establir una xarxa privada entre el client i el servidor.

![](img/1.png)  
![](img/2.png)  

### 3) Actualitzar el sistema
Actualitzarem la màquina per tenir tots els paquets al dia i evitar errors durant la instal·lació. Executa la següent comanda:

```bash
sudo apt update && sudo apt upgrade -y
```

![](img/3.png)  

### 4) Instal·lar el servei vsftpd
Ara instal·larem el servidor FTP **vsftpd**, que ens permetrà gestionar transferències de fitxers de manera senzilla.

```bash
sudo apt install vsftpd -y
```

![](img/4.png)  

### 5) Crear còpia de seguretat del fitxer de configuració
Abans de modificar res, farem una còpia del fitxer original per poder restaurar-lo si cal.

```bash
sudo cp /etc/vsftpd.conf /etc/vsftpd.conf.bak
```

![](img/5.png)  

### 6) Editar la configuració de vsftpd
Obrirem el fitxer de configuració amb **nano** per ajustar els paràmetres necessaris.

```bash
sudo nano /etc/vsftpd.conf
```

![](img/6.png)  

### 7) Comprovar estructura de fitxers
Farem un **tree** per verificar l’estructura dels directoris i assegurar-nos que tot està correctament organitzat.

![](img/7.png)  

### 8) Connexió FTP des del client
Des del client, establirem la connexió amb el servidor FTP utilitzant la seva IP interna.

```bash
ftp 192.168.56.101
```

![](img/8.png)  

### 9) Comprovació de fitxers
Un cop connectats, utilitzarem la comanda **dir** per veure el contingut del directori remot.

![](img/9.png)  

### 10) Analitzar tràfic amb Wireshark
Obrirem **Wireshark** per capturar i analitzar els paquets FTP que circulen per la xarxa, comprovant la seguretat i el flux de dades.

![](img/10.png)  

### 11) Preparar certificats SSL
Accedirem al directori de certificats per configurar FTP segur. Primer entrarem com a root i comprovarem els fitxers disponibles.

```bash
sudo su
ls /etc/ssl/private/
```

![](img/11.png)  

### 12) Configurar FTP segur
Modificarem les línies corresponents al fitxer `/etc/vsftpd.conf` per habilitar connexions segures amb SSL/TLS.

![](img/12.png)  

### 13) Verificació de connexió segura
Després dels canvis, intentarem connectar-nos de nou. Si la configuració és correcta, la connexió FTP sense seguretat ja no serà permesa.

![](img/13.png)  

### 14) Instal·lar FileZilla
Instal·larem el client gràfic **FileZilla** per gestionar les connexions FTP de manera més còmoda.

```bash
sudo apt install filezilla
```

![](img/14.png)  

### 15) Obrir FileZilla i acceptar connexió
Un cop obert, introduirem les dades del servidor i acceptarem la connexió FTP insegura per continuar amb les proves.

![](img/15.png)  

### 16) Connexió establerta
Finalment, comprovarem que la connexió amb el servidor s’ha realitzat correctament i podem transferir fitxers.

![](img/16.png)  
