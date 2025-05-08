# Uso de IntelliJ

**Para abrir el proyecto recién creado con IntelliJ IDEA.**

1. Desde el IntelliJ elegir la opción <shortcut>Open</shortcut> para abrir un nuevo proyecto

![intellij-archetype-1.png](intellij-archetype-1.png)

2. Desde el explorador de archivos emergente elegir el **pom.xml del directorio raíz del proyecto**.

En este ejemplo es <code>sample-project/pom.xml</code>

3. Elegir <shortcut>Open as Project</shortcut>

![intellij-archetype-2.png](intellij-archetype-2.png)

4. Desde el menú de <shortcut>Maven</shortcut> puede ejecutar los comandos <code>mvn clean</code> y
<code>mvn package</code> sin recurrir a la terminal

![intellij-archetype-3.png](intellij-archetype-3.png)

<tip>

Recordar de siempre seleccionar el módulo parent
(en este ejemplo <code>sample-project-parent</code>)

</tip>

## Solución de Problemas gRPC

<tip>

En el caso de que **el IDE no reconozca archivos autogenerados por el proyecto gRPC** recomendamos intentar
las siguientes opciones desde el menú contextual (click derecho) sobre el archivo **pom.xml del módulo padre**:

1. **Generate Sources and Update Folders**

2. **Sync Project**

![intellij-archetype-4.png](intellij-archetype-4.png)

**Si los problemas continúan:**

3. Dirigirse al directorio **api/target/generated-sources**
Debería ver un archivo terminado en Grpc correspondiente al servicio
(En este caso <code>TrainTicketServiceGrpc.java</code>) y archivos correspondientes
a los mensajes (como <code>Train.java</code> y <code>TrainOrBuilder.java</code>)

![intellij-archetype-5.png](intellij-archetype-5.png)

4. Para que todos estos archivos sean considerados como código fuente debemos
marcar manualmente el directorio.
- Sobre **api/target/generated-sources/protobuf/grpc-java** elegir 
<shortcut>Mark Directory as</shortcut> -> <shortcut>Generated Sources Root</shortcut>
- Repetir el mismo proceso para **api/target/generated-sources/protobuf/java**

![intellij-archetype-6.png](intellij-archetype-6.png)

Ahora el IDE debería mostrarle los archivos así:

![intellij-archetype-7.png](intellij-archetype-7.png)

Por último **repetir pasos 1 y 2** para que el IDE reconozca esos archivos.

</tip>

<warning>

<p>
En el caso de que se obtenga un error con el plugin protoc en macOS asegurarse de tener instalado Rosetta 2:
</p>

<p>
Para instalar Rosetta 2 correr el siguiente comando en la terminal
<code>softwareupdate --install-rosetta</code>
</p>

</warning>

## Solución de Problemas Cliente HTTP

<tip>

Si al utilizar el cliente HTTP integrado en el IntelliJ obtiene el siguiente error

<code>com.intellij.grpc.requests.RejectedRPCException: An error occurred during protocol buffers file binary assembly. Details are logged</code>

![intellij-http-1.png](intellij-http-1.png)

Dirigirse a <shortcut>Settings</shortcut> -> <shortcut>Languages \& Frameworks</shortcut> -> <shortcut>Protocol Buffers</shortcut>

![intellij-http-2.png](intellij-http-2.png)

En la sección Auto-Configuration Options tildar la opción
**Search for imported files in indexes**

![intellij-http-3.png](intellij-http-3.png)

Debería ver que se agrega nueva Location denominada **.proto files found in IDE indexes** 
en la sección Import Paths.
Ahora puede reintentar la ejecución del método.

![intellij-http-4.png](intellij-http-4.png)

</tip>
