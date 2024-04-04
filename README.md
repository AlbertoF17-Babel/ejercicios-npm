## Ejercicio 1 - Ejercicio de añadir dependencia con NPM
 
Crear proyecto con npm 

     npm init

Añadir una dependencia cualquiera

    npm i loglevel

Ver que se crea carpeta de dependencia en node_modules y se actualiza package.json
Revisar en ambos casos las versiones instaladas

## Ejercicio 2 - Ejercicio de añadir dependencia de versión específica con NPM

Añadir una versión específica de una dependencia

    npm i orm@7.0.0

Ver que se crea carpeta de dependencia en node_modules y se actualiza package.json. 
Revisar en ambos casos las versiones instaladas

## Ejercicio 3 - Actualización conjunta de proyecto

Crear un proyecto con npm y subirla a un repo (git) común.
Cada alumno debe añadir una dependencia (cada uno la que quiera) sobre el mismo proyecto usando gitflow.

El objetivo de este ejercicio es:
 - ver como interactúa la gestión de dependencias con git. 
 - Como podemos coordinarnos mediante git para la actualización de dependencias.
 - Como de sencillo es la sincronización de dependencias en un equipo, pero también trabajar la gestión de conflictos y merges en estos casos.

 Se trabaja tanto el entender el concepto de repositorio de dependencias, como SOBRE TODO el concepto de configuración centralizada

## Ejercicio 4 - Actualización de dependencia a última versión

Partir del ejercicio 2 y realizar una actualización automática

    npm update orm

Comprobar nuevas versiones en node_modules y package.json

## Ejercicio 5 - Actualización masiva de dependencias 

Añadir a proyecto 2 o más dependencias con versiones específicas que no sean la última.
Ejecutar

    npm update

Comprobar nuevas versiones en node_modules y package.json 
Pregunta: ¿Qué ha ocurrido?

## Ejercicio 6 - Actualización de dependencia a versión específica por línea de comandos

Añadir este paquete:

    npm i lodash@4.17.15

Comprobar nuevas versiones en node_modules y package.json - Debe haber actualizado todos los paquetes desactualizados
    (En node_modules ver .package-lock.json y lodash/lodash.js)

Actualizar a versión 4.17.16

    npm i lodash@4.17.16

Comprobar nuevas versiones en node_modules y package.json - Debe haber actualizado todos los paquetes desactualizados
    (En node_modules ver .package-lock.json y lodash/lodash.js)

## Ejercicio 7 - Actualización de dependencia a versión específica por fichero de configuración

Sobre ejercicio 6, cambiar versión de lodash en package.json a versión 4.17.17
La dependencia debe configurarse de esta forma: 

    "dependencies": {
        "lodash": "4.17.17"

    }

Para que los cambios sean efectivos ejecutar:

    npm install


## Ejercicio 8 - Actualización de dependencia a versión específica por fichero de configuración

Sobre el ejercicio 7, cambiar la configuración a esta forma:


     "dependencies": {
        "lodash": "^4.17.18"
    }

Ejecutar:

    npm install

Pregunta: ¿Qué versión va a instalar?

Pregunta: ¿Por qué? ¿Qué diferencia hay con el ejercicio 7?

Nota: Si la versión instalada cumple la condición de que es igual o superior a la solicitada no actualiza con npm install

## Ejercicio 9 - Downgrade de dependencia por línea de comandos

Sobre el ejercicio 8 Bajar a versión 4.17.16

Ejecutar:

    npm i lodash@4.17.16


## Ejercicio 10 - Hacer lo mismo del ejercicio 9 pero por fichero package.json


## Ejercicio 11 - Actualización de versión teniendo ya dependencia

Sobre ejercicio 9, actualizar a versión 4.17.18 con:

     npm i lodash@4.17.18

Si ahora cambiamos el fichero package.json a 

    "dependencies": {
        "lodash": "^4.17.16"
    }

y hacemos un:

    npm install

Pregunta: ¿Qué va a pasar?
