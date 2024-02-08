# LABORATORIO #2:  APLICACIONES DISTRIBUIDAS

Escriba un servidor web que soporte múlltiples solicitudes seguidas (no concurrentes). El servidor debe leer los archivos del disco local y retornar todos los archivos solicitados, incluyendo páginas html, archivos java script, css e imágenes. Construya una aplicación web con  javascript, css, e imágenes para probar su servidor. Incluya en la aplicación la comunicación asíncrona con unos servicios REST en el backend. NO use frameworks web como Spark o Spring, use solo Java y las librerías para manejo de la red.

## PREREQUISITOS

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
