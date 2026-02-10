# 📘 README — Pràctica Moodle (Escola Júlia)

## Breu descripció

Pràctica individual i tancada. L’objectiu és demostrar que saps **instal·lar, personalitzar, configurar i gestionar Moodle** com si fos un encàrrec real.  
El client és **l’Escola Júlia**, un centre de secundària que necessita un portal d’aprenentatge online.  
La pràctica té **5 parts** i cada part s’ha d’ensenyar i defensar davant del professorat.

***

# 🧩 Part 1 — Instal·lació i personalització del Moodle

*   Descomprimir Moodle al servidor web i iniciar la instal·lació.
*   Crear una base de dades **MySQL Improved** anomenada `moodle` (usuari root / contrasenya root).
*   Crear l’usuari administrador: **admin / Administrador\_1** + email + població + país.
*   Configurar l’idioma predeterminat en **català**.
*   Configurar la pàgina principal:
    *   Nom complet: *Escola d’Ensenyament Secundari Júlia*
    *   Nom curt: *Escola Júlia*
    *   Afegir descripció llarga (extreta d’una web real d’una escola).
    *   No mostrar res fins que l’usuari entri; després mostrar categories i buscador.
*   Instal·lar i aplicar **un tema nou**.
*   Afegir **favicon personalitzat** i, si el tema ho permet, **logo de l’escola**.

***

# 🧩 Part 2 — Creació d’usuaris i cursos

*   Crear categories: **1er ESO, 2on ESO, 3er ESO, 4rt ESO**.
*   Crear usuaris professors (segons arxiu adjunt 1).
*   Assignar Pedro Ruiz Gómez com a **creador de cursos** i donar-li permís per gestionar categories.

### Com a Pedro Ruiz Gómez:

Crear aquests cursos dins **1er ESO**:

1.  **Matemàtiques 1** (`MAT_1ESO`)
    *   Inici 12/09/2025
    *   Visible
    *   Resum (arxiu adjunt 2)
    *   Format de 5 temes, 1 per pàgina
    *   Idioma català
    *   5 notícies, qualificacions visibles
    *   Límits de fitxer 2MB
    *   Sense grups
    *   Nom del professor: **Senyor Ruiz**

2.  **Taulell d’anuncis 1** (`TAU_1ESO`)
    *   Inici 12/09/2025
    *   Visible
    *   Resum curt
    *   Format social
    *   Sense notícies ni qualificacions ni informes
    *   Fitxers màx 2MB

3.  **Informàtica 1** (`INF_1ESO`)
    *   Inici 12/09/2025
    *   Visible
    *   Resum (arxiu adjunt 3)
    *   Format 12 setmanes, una sola pàgina
    *   Temes ocults visibles
    *   Idioma català
    *   5 notícies + qualificacions + informes
    *   Treball en grups, visibilitat restringida
    *   Professor: **Senyor Ruiz**
    *   Professor no-editor: **Senyoreta Blazquez**

*   Ordenar cursos: el **Taulell d’anuncis 1** ha d’aparèixer primer.
*   Assignar professors i comprovar permisos.
*   Permetre **automatrícula**:
    *   Matemàtiques 1 → `mates1`
    *   Informàtica 1 → `info1`
*   El curs **Taulell d’anuncis 1** té accés de visitant → contrasenya `guest`.
*   Activar autenticació per **correu electrònic**.
*   Registrar un nou alumne i **confirmar-lo manualment** com a administrador.

***

# 🧩 Part 3 — Afegir contingut al curs Matemàtiques 1

Com a **Pedro Ruiz Gómez**:

1.  Afegir títol i resum als 5 temes (Nombres, Equacions 1r grau, Equacions 2n grau, Polinomis, Trigonometria).
2.  Afegir una **etiqueta inicial** amb nom del curs + imatge.
3.  Afegir un **fòrum**: *Fòrum de Matemàtiques 1*.
4.  Afegir un **glossari** + 3 entrades (mínim una amb imatge).
5.  Afegir un **xat** amb sessions setmanals dissabte a les 10:00.
6.  Afegir una **enquesta COLLES** → *Enquesta de satisfacció*.
7.  Afegir enllaç URL → *XTEC - Matemàtiques*.
8.  Afegir una **pàgina** amb taula de criteris d’avaluació.
9.  Reordenar: etiqueta → enllaç → pàgina → fòrum → xat → glossari → enquesta.

***

# 🧩 Part 4 — Activitats complexes al curs Matemàtiques 1

1.  Dividir el tema **Nombres** en 3 etiquetes: *Apunts*, *Exercicis pràctics*, *Exercicis d’avaluació* (totes amb imatge).
2.  Afegir una **consulta** amb operació matemàtica i respostes 5, 9 i 18.
3.  Afegir una **lliçó**: *Els nombres racionals*
    *   Barra de progrés, puntuació, menú 75%
    *   Format presentació
    *   4 pàgines de contingut + 4 preguntes V/F
4.  Afegir un **qüestionari**: *Exercici d’avaluació 1*
    *   Disponible 25 de febrer, 9–10h
    *   20 minuts
    *   Preguntes barrejades
    *   5 preguntes de diferents tipus
    *   Penalització 25%
    *   Retroaccions globals
5.  Afegir **tasca text en línia**: *Exercici pràctic 2*.
6.  Afegir **tasca de fitxer**: *Exercici d’avaluació 2*, límit 25 febrer 10h.

***

# 🧩 Part 5 — Plugins, blocs i còpies de seguretat

Com a administrador:

1.  Afegir blocs:
    *   **Calendari**
    *   **Esdeveniments pròxims**
    *   **Usuaris en línia**
    *   **Mis cursos**
    *   **Comentaris**
    *   **Entrada aleatòria de glossari** (del glossari del curs)
    *   **Canal RSS remot** (El Periódico + La Vanguardia)
    *   **Text** (amb enllaços a XTEC / Recursos TIC / Vitutor)
    *   Configurar visibilitat:
        *   Calendari + Esdeveniments → a tot el curs
        *   La resta → només pàgina principal del curs
2.  Afegir gadgets via blocs de text:
    *   Un rellotge JavaScript
    *   Un gadget web (qualsevol).
3.  Crear **3 insígnies** amb Canva i assignar-les a 3 activitats (seguiment activat).
4.  Fer una **còpia de seguretat** del curs Matemàtiques 1 i restaurar-la com:
    *   *Matemàtiques 1 backup* — nom curt *MAT\_BCKP*.

***