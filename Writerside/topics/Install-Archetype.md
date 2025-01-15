# Instalación del arquetipo

Un **arquetipo** es un proyecto de Maven que permite generar proyectos a partir de un template.

1. Descargar <resource src="pod-grpc-archetype.zip"/>, **descomprimirlo** y **pararse sobre el directorio recién creado**

<tabs>
    <tab id="macos-unzip" title="macOS">
        <code-block lang="console">
            user@Users-MacBook-Pro ~ % unzip pod-grpc-archetype.zip
            ...
            user@Users-MacBook-Pro ~ % cd pod-archetype/
        </code-block>
    </tab>
    <tab id="linux-unzip" title="Linux">
        <code-block lang="console">
            user@host:~$ unzip pod-grpc-archetype.zip
            ...
            user@host:~$ cd pod-archetype/
        </code-block>
    </tab>
    <tab id="windows-unzip" title="Windows">
        <p>Luego de finalizada la descarga ubicar el archivo correspondiente.</p>
        <p>En el explorador de archivos, usando el menú contextual sobre la descarga elegir la opción Extraer todo...</p>
        <p>Elegir un path donde deseemos descomprimir el arquetipo de Maven. En este caso utilizaremos</p>
        <shortcut>C:\Maven</shortcut>
        <p>Se creará la carpeta necesaria.</p>
        <img src="windows-maven-0.png" alt="Windows 0" width="600"/>
        <p>En el explorador de archivos, usando el menú contextual sobre el directorio pod-archetype recién creado la opción Abrir en Terminal</p>
        <p>La ventana de la terminal debería ubicada en el siguiente directorio</p>
        <shortcut>C:\Maven\pod-archetype</shortcut>
</tab>
</tabs>

2. Desde la consola, sobre el directorio recién descomprimido, correr el siguiente comando

<code-block lang="console">mvn clean install</code-block>

Debería obtener una salida similar a la siguiente

<code-block lang="console">
[INFO] --- archetype:2.4:update-local-catalog (default-update-local-catalog) @ pod-mp-grpc-archetype ---
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  14.804 s
[INFO] Finished at: 2025-01-15T16:08:43-03:00
[INFO] ------------------------------------------------------------------------
</code-block>

3. Para actualizar el índice local con información sobre los arquetipos disponibles correr el siguiente comando

<code-block lang="console">mvn archetype:crawl</code-block>

<note>
    <p>
        Listo! Ya cuenta con el arquetipo instalado correctamente.
    </p>
</note>