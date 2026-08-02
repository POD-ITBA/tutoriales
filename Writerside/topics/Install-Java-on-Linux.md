# Instalación de Java en Linux

<warning>
    <p>
        Es necesario contar con el gestor de paquetes <a href="https://snapcraft.io"><b>Snap</b></a> 
    </p>
</warning>

## Uso de snap

Puede verificar la instalación de **snap** utilizando el siguiente comando

<code-block lang="console">snap --version</code-block>

donde debería obtener una salida como la siguiente

<code-block lang="plain text">
snap          2.76.1
snapd         2.76.1
series        16
ubuntu        26.04
kernel        7.0.0-28-generic
architecture  arm64
</code-block>

## Instalación de OpenJDK

A continuación debe instalar el paquete
<code>openjdk</code>

Instale el paquete con el siguiente comando

<code-block lang="console">sudo snap install openjdk</code-block>

## Alias

Se debe editar el archivo con la configuración del intérprete **Bash** para
definir las variables de entorno necesarias.

Para aplicarlo en el **usuario actual** modificar el archivo <shortcut>~/.bashrc</shortcut>

Para aplicarlo en **todos los usuarios** modificar el archivo <shortcut>/etc/bash.bashrc</shortcut>

Abrir el archivo y agregar dos renglones al final con los siguientes comandos:

<code-block lang="console">
source $(openjdk)
export PATH=$JAVA_HOME/bin:$PATH
</code-block>

Guardar los cambios del archivo. 

Las variables de entorno estarán listas la próxima vez que abra una terminal.

## Consultar la versión instalada

Consulte la versión de Java instalada

<code-block lang="console">java -version</code-block>

Debería ver una salida similar a la siguiente

<code-block lang="plain text">
user@host:~$ java -version
openjdk version "26.0.1" 2026-04-21
OpenJDK Runtime Environment (build 26.0.1+8-snap)
OpenJDK 64-Bit Server VM (build 26.0.1+8-snap, mixed mode, sharing)
</code-block>

Identifique en la salida una versión
<shortcut>25</shortcut> o superior, en este ejemplo es la <code>26.0.1</code>

<note>
    <p>
        Listo! Ya cuenta con Java instalado correctamente.
    </p>
</note>
