# Ejecución de server y client

Para conseguir los scripts de ejecución (tanto el proyecto **server** como **client**) se debe realizar una serie de pasos.

<warning>
    <p>
        Para los usuarios de <b>Windows</b> se recomienda contar con la terminal <a href="https://git-scm.com/downloads/win"><b>Git Bash</b></a>
        para poder ejecutar comandos de bash directamente desde Windows sin WSL. 
    </p>
    <p>
        Una vez instalado, en lugar de abrir la Consola de Windows abra la aplicación Git Bash y ejecute allí los comandos que se listan a continuación 
    </p>
</warning>


A continuación se explica un ejemplo para el módulo server del proyecto sample-project pero el mismo debe repetirse también para el client/ correspondiente.

1. Ubicarse en el directorio **target/**

<code-block lang="console">
cd server/target/
</code-block>

2. **Descomprimir** el archivo con extensión **tar.gz**

<code-block lang="console">
tar -xzf sample-project-server-1.0-SNAPSHOT-bin.tar.gz
</code-block>

3. Ubicarse en el directorio recién creado

<code-block lang="console">
cd sample-project-server-1.0-SNAPSHOT
</code-block>

4. Dar **permisos de ejecución** a los scripts .sh ubicados en el directorio recién creado

<code-block lang="console">
chmod u+x *.sh
</code-block>

5. **Ejecutar** el script correspondiente

<code-block lang="console">
sh run-server.sh    
</code-block>

<warning>
    <p>
        En caso de obtener un error como
    </p>
    <code-block>
    Error: Could not find or load main class ar.edu.itba.pod.server.Server
    Caused by: java.lang.ClassNotFoundException: ar.edu.itba.pod.server.Server
    </code-block>
    <p>
        1. Asegurarse de estar ubicado en el mismo directorio del script.
    </p>
    <p>
        2. Consultar la siguiente sección Modificación de los scripts
    </p>
</warning>

<note>
    <p>
        Listo! Ya puede ejecutar el server desde la terminal correctamente.
    </p>
    <p><b>
        Repita el mismo procedimiento para el módulo client desde otra terminal.
    </b></p>
</note>

## Modificación de los scripts

En caso de querer **que el script ejecute una clase distinta** a la indicada por defecto
basta con **modificar el .sh correspondiente** ubicado en el directorio assembly/overlay/.

Por ejemplo para el módulo **server** el archivo **run-server.sh** se encuentra ubicado en

<shortcut>
src/main/assembly/overlay/run-server.sh
</shortcut>

A continuación el contenido del run-server.sh que se obtiene al crear un nuevo proyecto

<code-block lang="bash">
#!/bin/bash

PATH_TO_CODE_BASE=`pwd`
MAIN_CLASS="ar.edu.itba.pod.server.Server"

java  $JAVA_OPTS -cp 'lib/jars/*' $MAIN_CLASS $*
</code-block>

Puede cambiar <shortcut>MAIN_CLASS</shortcut> por el FQN (Fully Qualified Name) de la clase que desee.

<tip>
    <p>
        Recordar de volver a ejecutar 
        <b>mvn install</b> luego de realizar cambios en los scripts de assembly/
        para que estos cambios se vean reflejandos en los scripts de target/
    </p>
</tip>
