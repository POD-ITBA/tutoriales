# Nuevo proyecto desde la terminal

Para crear un **nuevo proyecto** utilizando un arquetipo.

<warning>

Asegurarse de estar ubicado en un **directorio distinto al del pod-archetype/**

</warning>

1. Ejecutar el siguiente comando

<code-block lang="console">mvn archetype:generate -DarchetypeCatalog=local
</code-block>

2. Aparecerá un menú de opciones. Escribir la opción correspondiente al arquetipo de <shortcut>pod</shortcut>
y presionar <shortcut>Enter</shortcut>

En este caso es la opción <shortcut>1</shortcut>.

<code-block lang="console">
[INFO] Generating project in Interactive mode
[INFO] No archetype defined. Using maven-archetype-quickstart (org.apache.maven.archetypes:maven-archetype-quickstart:1.0)
Choose archetype:
1: local -> ar.edu.itba.pod:pod-mp-grpc-archetype (pod)
Choose a number or apply filter (format: [groupId:]artifactId, case sensitive contains): : 
</code-block>

3. Completar los valores pedidos de <code>groupId</code>, <code>artifactId</code>, <code>version</code> y <code>package</code>
y por último presionar <shortcut>Y</shortcut>.

Para version y package puede presionar <shortcut>Enter</shortcut> y así tomar el valor por defecto.

<code-block lang="console">
Define value for property 'groupId': ar.edu.itba.pod
Define value for property 'artifactId': sample-project
Define value for property 'version' 1.0-SNAPSHOT: 
Define value for property 'package' ar.edu.itba.pod: 
Confirm properties configuration:
groupId: ar.edu.itba.pod
artifactId: sample-project
version: 1.0-SNAPSHOT
package: ar.edu.itba.pod
 Y: Y
</code-block>

4. Debe ver en la salida el **Build Sucess** indicando la ubicación de los pom.xml recién creados. Por ejemplo:

<code-block lang="console">
[INFO] Parent element not overwritten in /Users/foo/sample-project/api/pom.xml
[INFO] Parent element not overwritten in /Users/foo/sample-project/server/pom.xml
[INFO] Parent element not overwritten in /Users/foo/sample-project/client/pom.xml
[INFO] Project created from Archetype in dir: /Users/foo/sample-project
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  04:10 min
[INFO] Finished at: 2025-01-15T16:42:30-03:00
[INFO] ------------------------------------------------------------------------
</code-block>

5. Ubicarse en el directorio recién creado (en este caso <code>sample-project/</code>) 
y correr el comando <code>mvn clean install</code> sobre el pom padre.

<tabs>
    <tab id="macos-new-project" title="macOS">
        <code-block lang="console">
            user@Users-MacBook-Pro ~ % cd sample-project 
            user@Users-MacBook-Pro sample-project % mvn clean install
        </code-block>
    </tab>
    <tab id="linux-new-project" title="Linux">
        <code-block lang="console">
            user@host:~$ cd sample-project/
            user@host:~/sample-project$ mvn clean install
        </code-block>
    </tab>
    <tab id="windows-new-project" title="Windows">
        <code-block lang="console">
            C:\Users\Foo\Desktop>cd sample-project
            C:\Users\Foo\Desktop\sample-project>mvn clean install
        </code-block>
    </tab>
</tabs>

Debería obtener una salida similar a la siguiente:

<code-block lang="console">
[INFO] ------------------------------------------------------------------------
[INFO] Reactor Summary for sample-project-parent 1.0-SNAPSHOT:
[INFO]
[INFO] sample-project-parent .............................. SUCCESS [  1.173 s]
[INFO] sample-project-api ................................. SUCCESS [ 26.145 s]
[INFO] sample-project-server .............................. SUCCESS [  2.119 s]
[INFO] sample-project-client .............................. SUCCESS [  0.546 s]
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  34.575 s
[INFO] Finished at: 2025-01-15T16:46:43-03:00
[INFO] ------------------------------------------------------------------------
</code-block>
