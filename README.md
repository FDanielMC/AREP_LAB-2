# LABORATORIO #2:  APLICACIONES DISTRIBUIDAS

Escriba un servidor web que soporte múlltiples solicitudes seguidas (no concurrentes). El servidor debe leer los archivos del disco local y retornar todos los archivos solicitados, incluyendo páginas html, archivos java script, css e imágenes. Construya una aplicación web con  javascript, css, e imágenes para probar su servidor. Incluya en la aplicación la comunicación asíncrona con unos servicios REST en el backend. NO use frameworks web como Spark o Spring, use solo Java y las librerías para manejo de la red.

### PREREQUISITOS

* [Java (desde la 15 para delante)](https://www.oracle.com/co/java/technologies/downloads/) 
* [Maven](https://maven.apache.org/download.cgi) 
* [Git](https://git-scm.com/downloads) 

### REQUISITOS

1. Contar con IDE para la ejecución del proyecto o línea de comandos.
2. Contar con los prerequisitos.
3. Al tenerlos, ejecutar el siguiente comando en la maquina

```bash
git clone https://github.com/FDanielMC/AREP_LAB-2.git
```

### JAVADOC
Usando el siguiente comando se genera la documentación del proyecto y para acceder a ella se encuentra en la carpeta targe/site en el archivo index.html: 
```
mvn site
```
En caso que no aparezcan el JAVADOC luego de haber ejecutado ese comando se puede hacer mediante NETBEANS:
![image](https://github.com/FDanielMC/AREP_LAB-2/assets/123689924/c8aee78f-38c4-4a63-ad28-016ee38f8598)
![image](https://github.com/FDanielMC/AREP_LAB-2/assets/123689924/839db2ca-8927-4eb3-b217-057808a54ed0)


### DESCRIPCION DEL PROYECTO

El programa consta por 4 clases java. La clase Main es la que pondra en funcionamiento todo el programa, la clase MovieClient pondra en ejecución el servidor web que retorna las páginas necesarias para poder realizar la búsqueda de las películas. Por medio de la clase OMDBProvider se realizan las peticiones correspondientes a la API externa y una clase Cache para almacenar las peticiones que ya se han realizado, así usando un buen uso de los recursos.

Para la parte del FrontEnd se añadieron archivos con extensión .html, .css y .js. Luego de haber ejecutado el programa y buscarlo en el browser se verá de la siguiente manera:

![image](https://github.com/FDanielMC/AREP_LAB-2/assets/123689924/83e7815c-a615-4ba5-913b-d797425fabdf)


## INICIANDO EL PROYECTO

```
1. En un IDE de desarrollo o en la línea de comandos se ejecuta la clase Main.java, se recomienda hacerlo desde la línea de comandos. 
2. En un browser, ingresar a la URL http://localhost:35000
3. En la barra de busqueda, insertar el nombre de la pelicula a buscar
```

Si desea hacerlo usando la linea de comandos, use los siguientes comandos (se recomienda hacerlo de esta manera):
```
mvn clean compile
mvn exec:java
```

## EJECUTAR PRUEBAS

Para ejecutar las pruebas ingrese el siguiente comando en la línea de comandos:
```
mvn test
```

### Añadidos del proyecto

Se agregaron los archivos para el front, los ".html", "css/.css" y "js/.js". Además se agregó la opción de poder buscar imágenes del servidor. Las imágenes se encuentran en la carpeta "img". El código HTML estaba principalmente en la clase MovieClient, por lo que la misma clase MovieClient generaba el cuerpo de las páginas, por lo que se modificó MovieClient para que obtenga los archivos .html, .css, .js, .png y .jpg para así obtener el contenido de cada archivo para luego volverlos texto plano o bytes según el tipo de archivo que fuera.

![image](https://github.com/FDanielMC/AREP_LAB-2/assets/123689924/ada73271-ef1b-4c70-ae89-23a692f3af05)

![image](https://github.com/FDanielMC/AREP_LAB-2/assets/123689924/f2d14b35-b9ad-44fb-9b73-ce31a9b7a56a)

![image](https://github.com/FDanielMC/AREP_LAB-2/assets/123689924/6bd4aead-5edb-409c-acb1-074a40bef437)

![image](https://github.com/FDanielMC/AREP_LAB-2/assets/123689924/890b3cdd-90df-4077-a105-3b4de41d9833)

## DESARROLLADO CON

* [Java version 15 (Netbeans JDK 15)](https://www.oracle.com/co/java/technologies/downloads/)
* [Maven](https://maven.apache.org/download.cgi)
* [Git](https://git-scm.com/downloads)
* [omdbapi](https://www.omdbapi.com)

## Autor

* **Daniel Fernando Moreno Cerón** - [FDanielMC](https://github.com/FDanielMC)

### Licencia

This project is licensed under the MIT License - see the LICENSE.md file for details

### Agradecimientos

Escuela Colombiana de Ingeniería
