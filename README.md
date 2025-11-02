# Informe Técnico: Introducción a Docker
**Autor:** [Luis sneider Gonzalez]  

---

##  1. Resumen de los conceptos aprendidos en cada video

###  Video 1: [Introducción a Docker](https://www.youtube.com/watch?v=CV_Uf3Dq-EU)

**Conceptos principales:**
- **Qué es Docker:** Plataforma que permite empaquetar aplicaciones y sus dependencias dentro de contenedores portátiles.
- **Diferencia entre máquina virtual y contenedor:** Los contenedores comparten el mismo kernel del sistema operativo, lo que los hace más ligeros y rápidos que las máquinas virtuales.
- **Imágenes vs contenedores:**  
  - *Imagen:* plantilla inmutable con el entorno y la aplicación.  
  - *Contenedor:* instancia ejecutándose de una imagen.  
- **Comandos básicos:**  
  - `docker run hello-world` para probar la instalación.  
  - `docker ps` para listar contenedores activos.  
  - `docker stop` y `docker rm` para detener y eliminar contenedores.  
- **Ventajas:** portabilidad, consistencia del entorno, despliegue rápido y fácil distribución mediante Docker Hub.

---

###  Video 2: [Creación y uso de imágenes Docker](https://www.youtube.com/watch?v=4Dko5W96WHg)

**Conceptos principales:**
- **Dockerfile:** archivo de texto con instrucciones para crear una imagen personalizada (`FROM`, `RUN`, `COPY`, `WORKDIR`, `CMD`, etc.).
- **Construcción de imágenes:**  
  - Comando `docker build -t nombre_imagen .`  
  - Uso de capas para mantener eficiencia y tamaño reducido.  
- **Volúmenes:** permiten que los datos persistan aunque el contenedor se elimine.  
- **Redes:** los contenedores pueden comunicarse entre sí o con el host mediante redes creadas con Docker.  
- **Puertos:** se exponen con `-p` (por ejemplo `-p 8080:80`) para acceder a los servicios.  
- **Buenas prácticas:**  
  - Usar imágenes base ligeras (como `alpine`).  
  - Limpiar archivos temporales.  
  - Versionar imágenes y usar etiquetas (`tags`).  
- **Ejemplo práctico:** despliegue de una aplicación simple dentro de un contenedor, mostrando cómo se ejecuta igual en cualquier máquina con Docker instalado.

---

##  2. Reflexiones personales

###  Ventajas
- **Portabilidad total:** la aplicación se ejecuta igual sin importar el sistema operativo o la configuración local.  
- **Rapidez y ligereza:** arranque en segundos gracias al uso del kernel compartido.  
- **Escalabilidad:** facilita crear y mantener aplicaciones modulares basadas en microservicios.  
- **Entornos reproducibles:** ideal para equipos de desarrollo y DevOps.

---

###  Desafíos
- **Persistencia de datos:** si no se configuran volúmenes, los datos se pierden al eliminar un contenedor.  
- **Seguridad:** un contenedor mal configurado podría comprometer el sistema host.  
- **Gestión de redes y múltiples contenedores:** se complica a medida que los proyectos crecen.  
- **Tamaño de imágenes:** un Dockerfile mal diseñado puede generar imágenes demasiado pesadas.

---

###  Aplicación práctica personal
- En mis proyectos de **bases de datos e inventario**, Docker puede ayudarme a crear entornos listos para pruebas sin afectar mi sistema local.  
- Puedo crear un entorno completo con base de datos, backend y frontend usando contenedores separados.  
- Planeo practicar con **Docker Compose** para automatizar la ejecución de varios servicios simultáneamente.  
- Aplicar buenas prácticas desde el inicio: imágenes ligeras, manejo de volúmenes y versiones seguras.

---

##  3. Conclusión
Los dos videos me permitieron comprender los fundamentos de Docker y cómo aplicarlo en proyectos reales.  
El primero me enseñó **qué es Docker y por qué usarlo**, mientras que el segundo me mostró **cómo construir mis propias imágenes y contenedores**.  

Con esta herramienta puedo mejorar mis proyectos al hacerlos **más portables, eficientes y fáciles de desplegar**.  
Mi siguiente paso será crear un **proyecto práctico** usando un Dockerfile propio y levantar un entorno completo con varios contenedores.

---

 *Docker se convierte así en una pieza clave para el desarrollo moderno, especialmente en entornos colaborativos y proyectos de despliegue continuo (CI/CD).*
