# 📘 README — Desplegament de Directori Actiu (TransLògic S.A.)

## Introducció

Com a continuació de la tasca anterior amb Windows Server 2025, ara toca **desplegar el Directori Actiu** a la màquina virtual.  
Aquesta instal·lació serveix per:

*   Practicar el procediment abans d’anar al client.
*   Crear una **prova de concepte (PoC)** per ensenyar als responsables de TransLògic.
*   Ajustar la configuració a les necessitats reals de TransLògic S.A.

## Procediment a documentar

En la guia haureu de documentar aquests passos:

*   Instal·lar els **rols necessaris** al servidor (AD DS i els que pertoquin).
*   Crear un **domini nou en un bosc nou** amb el nom:  
    `translogicXX.test` (on `XX` és el vostre número de llista).
*   Establir el **nivell funcional** del bosc i del domini a **2025**.
*   Promocionar el servidor com a **controlador de domini**:
    *   Important: documentar la **pantalla de resum** de la promoció.
    *   Desar en un arxiu l’**script PowerShell** que automatitza el procés.

Un cop acabat:

*   Copiar l’script PowerShell al repositori que esteu utilitzant.
*   El podeu copiar mitjançant:
    *   USB
    *   Enviant-lo per Internet (correu, Drive, serveis de transferència)
    *   Usant `scp` (cal tenir SSH instal·lat a Windows Server)

## Materials i links de suport

*   Guia **UD6.AA3 Instal·lació DC** — Moodle SOX

***