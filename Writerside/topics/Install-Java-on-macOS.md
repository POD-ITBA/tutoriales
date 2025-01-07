# Instalación de Java en macOS

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

<code-block lang="plain text">Homebrew 4.4.15</code-block>

## Instalación de OpenJDK

A continuación debe instalar el paquete
<code>openjdk</code>

Instale el paquete con el siguiente comando

<code-block lang="console">brew install openjdk</code-block>

## Consultar la versión instalada

Consulte la versión de Java instalada

<code-block lang="console">java -version</code-block>

Debería ver una salida similar a la siguiente

<code-block lang="plain text">
user@Users-MacBook-Pro ~ % java -version    
openjdk version "23.0.1" 2024-10-15
OpenJDK Runtime Environment (build 23.0.1+11-39)
OpenJDK 64-Bit Server VM (build 23.0.1+11-39, mixed mode, sharing)
</code-block>

Identifique en la salida una versión
<shortcut>23</shortcut> o superior, en este ejemplo es la <code>23.0.1</code>

<note>
    <p>
        Listo! Ya cuenta con Java instalado correctamente.
    </p>
</note>