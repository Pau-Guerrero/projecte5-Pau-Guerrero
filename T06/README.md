# 📘 README — Desplegament d’OU, grups i usuaris del domini (TransLògic S.A.)

## Introducció

Un cop creat el domini, el següent pas és **desplegar-lo**: crear grups, usuaris, equips i estructurar-ho tot amb **unitats organitzatives (OU)**.  
Això permet ordenar els objectes del domini i facilita la gestió posterior.

## Procediment pràctic

*   Crear una **estructura d’OU coherent** i justificar-la.

*   Definir els grups:
    *   `gestio`
    *   `magatzem`
    *   `gerencia`
    *   `personal` (inclou els tres anteriors com a membres)

*   Crear una **plantilla d’usuari per cada grup**:
    *   Gestio
    *   Magatzem
    *   Gerencia  
        Cada plantilla ha d’incloure la pertinença al grup i la creació de la carpeta personal.

*   Crear **un usuari de prova** per cada plantilla.

*   Aprovisionar un equip anomenat **PC1** dins l’OU `equips`.

*   Crear una VM amb **Windows 11**, 4 GB de RAM i disc suficient. Xarxa en **NAT**.  
    Un cop creada, afegir-la al **domini**.

*   Comprovar que tot funciona iniciant sessió al client Windows 11 amb els **tres usuaris de prova**.

## Materials i links de suport

*   UD6.AA3 Desplegament — Moodle 0224 SOX

***