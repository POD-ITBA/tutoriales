# Instalación de Maven en macOS

<warning>
    <p>
        Es necesario contar con el gestor de paquetes
        <a href="https://brew.sh/es/">Homebrew</a> 
    </p>
    <p>
        Consulte el sitio web para su instalación.
    </p>
</warning>

## Uso de Homebrew

Puede verificar la instalación de **HomeBrew** utilizando el siguiente comando

<code-block lang="console">brew -v</code-block>

donde debería obtener una salida como la siguiente

<code-block lang="plain text">Homebrew 6.0.14</code-block>

## Instalación de Maven

A continuación debe instalar el paquete
<code>maven</code>

Instale el paquete con el siguiente comando

<code-block lang="console">brew install maven</code-block>

## Consultar la versión instalada

Consulte la versión de Maven instalada

<code-block lang="console">mvn -version</code-block>

Debería ver una salida similar a la siguiente

<code-block lang="plain text">
user@Users-MacBook-Pro ~ % mvn -version 
Apache Maven 3.9.16 (2bdd9fddda4b155ebf8000e807eb73fd829a51d5)
Maven home: /opt/homebrew/Cellar/maven/3.9.16/libexec
Java version: 26.0.2, vendor: Homebrew, runtime: /opt/homebrew/Cellar/openjdk/26.0.2/libexec/openjdk.jdk/Contents/Home
Default locale: es_AR, platform encoding: UTF-8
OS name: "mac os x", version: "26.6", arch: "aarch64", family: "mac"
</code-block>

Identifique en la salida una versión
<shortcut>3.9</shortcut> o superior, en este ejemplo es la <code>3.9.16</code>

<note>
    <p>
        Listo! Ya cuenta con Maven instalado correctamente.
    </p>
</note>

<seealso>
<!--Give some related links to how-to articles-->
</seealso>
