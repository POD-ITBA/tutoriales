# Instalación de Maven en Linux

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

## Instalación de Maven

A continuación debe instalar el paquete
<code>strictly-maven</code>

Instale el paquete con el siguiente comando

<code-block lang="console">sudo snap install strictly-maven</code-block>

## Alias

Se debe editar el archivo con la configuración de la terminal para
definir el alias necesario. En este caso se usará el editor **Vim**
para modificar las propiedades del intérprete **Bash**.

Abrir el archivo <shortcut>.bash_aliases</shortcut>

<code-block lang="console">vim ~/.bash_aliases</code-block>

Agregar un renglón al final del archivo con el siguiente comando

<code-block lang="console">alias mvn='strictly-maven'</code-block>

Guardar los cambios del archivo.

Las variables de entorno estarán listas la próxima vez que abra una terminal.

## Consultar la versión instalada

Consulte la versión de Maven instalada

<code-block lang="console">mvn -version</code-block>

Debería ver una salida similar a la siguiente

<code-block lang="plain text">
user@host:~$ mvn -version
Apache Maven 3.9.16 (2bdd9fddda4b155ebf8000e807eb73fd829a51d5)
Maven home: /snap/strictly-maven/37/maven
Java version: 26.0.1, vendor: Snap Build, runtime: /snap/strictly-maven/37/jdk
Default locale: es_ES, platform encoding: UTF-8
OS name: "linux", version: "7.0.0-28-generic", arch: "aarch64", family: "unix"
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

