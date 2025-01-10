# Instalación de Maven en Windows

## Descarga de Maven

Ir al sitio de
<a href="https://maven.apache.org/download.cgi"><b>Maven</b></a>
y descargar **Binary Zip Archive**

Luego de finalizada la descarga ubicar el archivo correspondiente. En este caso

<shortcut>apache-maven-3.9.9-bin.zip</shortcut> 

En el explorador de archivos, usando el menú contextual sobre la descarga elegir la opción **Extraer todo...**

Elegir un path donde deseemos instalar Maven. En este caso utilizaremos

<shortcut>C:\Maven</shortcut> 

Se creará la carpeta necesaria.

<img src="windows-maven-0.png" alt="Windows 0" width="600"/>

## Variables de entorno

Abrir **Configuración**. Luego en **Sistema**, elegir el botón **Información**

En la sección **Especificaciones del dispositivo** elegir la opción **Configuración avanzada del sistema**

En la ventana elegir la opción **Variables de entorno..** que se encuentra en la esquina inferior derecha.

En la sección **Variables del sistema** debe agregar una nueva variable de sistema presionando el botón **Nueva..**

En el popup completamos con <shortcut>M2_HOME</shortcut> como **Nombre de la variable**.
En **Valor de la variable** lo completamos con la opción **Examinar directorio...**

Elegir el path donde se instaló Java, en este caso, <shortcut>C:\Maven\apache-maven-3.9.9</shortcut>

<img src="windows-maven-1.png" alt="Windows 1" width="600"/>

Repetimos el proceso pero ahora para la variable de sistema <shortcut>MAVEN_HOME</shortcut>

<img src="windows-maven-2.png" alt="Windows 2" width="600"/>

Por último vamos a modificar la variable de sistema **Path** para que incluya a la recién definida

Seleccionar la variable de sistema Path y luego **Editar...**

En la ventana elegir la opción **Nuevo** y completar con
<shortcut>% M2_HOME%\bin</shortcut>

<img src="windows-maven-3.png" alt="Windows 3" width="600"/>

Aceptar los cambios en todas las ventanas.

## Consultar la versión instalada

Consulte la versión de Maven instalada
abriendo una terminal usando Símbolo de Sistema
y ejecutando el siguiente comando

<code-block lang="console">mvn -version</code-block>

Debería ver una salida similar a la siguiente

<code-block lang="plain text">
C:\Users\foo>mvn -version    
Apache Maven 3.9.9 (8e8579a9e76f7d015ee5ec7bfcdc97d260186937)
Maven home: C:\Maven\apache-maven-3.9.9
Java version: 23.0.1, vendor: Oracle Corportation, runtime: C:\Java\jdk-23.0.1
Default locale: es_ES, platform encoding: UTF-8
OS name: "windows 11", version: "10.0", arch: "amd64", family: "windows"
</code-block>

Identifique en la salida una versión
<shortcut>23</shortcut> o superior, en este ejemplo es la <code>23.0.1</code>

<note>
    <p>
        Listo! Ya cuenta con Java instalado correctamente.
    </p>
</note>