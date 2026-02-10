# 📘 README — Instal·lació de Windows Server 2025 (Cas TransLògic S.A.)

## Introducció al cas

TransLògic S.A. ens encarrega el desplegament dels seus Windows Server 2025.  
Abans d’implantar res al client, farem una **instal·lació de prova** en màquina virtual. Aquesta prova servirà per aprendre el procediment i per crear una **guia d’instal·lació** que utilitzarem en el desplegament final.

## Procediment

*   Crear una màquina virtual amb **8 GB de RAM**, **2 processadors**, **2 discos** (32 GB per al SO i 10 GB secundari).
*   Afegir **dues interfícies de xarxa**: una en NAT i una en **host‑only**.
*   Instal·lar **Windows Server 2025 GUI**, idioma US i teclat/configuració en espanyol.
*   Canviar el nom de l’equip a **DCxx** (xx = número de llista).
*   Actualitzar la màquina i **pausar actualitzacions** tant com sigui possible.

## Contingut de la guia

La guia d’instal·lació ha d’incloure:

*   Comparació entre la configuració de la VM i els requisits oficials de Microsoft.  
    → S’ha d’indicar si és coherent o no.
*   Documentació del procés d’instal·lació.  
    → **Captures de pantalla** i **observacions**.  
    → Format **Markdown** obligatori.

## Materials i links de suport

*   UD.6. AA2. Instal·lació Windows Server 2025 — Moodle (0224 Sist. Operatius en Xarxa)
*   Requisits de hardware per Windows Server — **Microsoft Learn**

***