## ArtBlock - Infraestructura y Despliegue
En esta parte de la aplicación tenemos, de manera ordenada, la configuración de los entornos de desarrollo y también la estrategia de despliegue en producción de la infraestructura del ecosistema ArtBlock. Esta separación entre el código fuente y la infraestructura viene determinado por el hecho de que cumplimos, en definitiva, con los patrones de arquitectura basada en servicios y el alto desacoplamiento.

## Entorno de Desarrollo Local (Docker)
Para el desarrollo lEl archivo docker-compose.yml incluido en este repositorio levanta una instancia de PostgreSQL lista para conectarse con el Backend.


## Tecnologias y Herramientas
Docker y Docker Compose instalados.

## Levantar la Base de Datos Local
Abre una terminal de bash  en la raíz de este repositorio.
docker-compose up -d
La base de datos estará disponible en el puerto local definido (usualmente 5432 o 5433).

Para detener el contenedor, utiliza:
docker-compose downocal

## Estrategia de Despliegue en Producción
Fronten en Vercel:	Alojamiento de la aplicación Next.js. Provee CDN global, Server-Side Rendering (SSR) optimizado y despliegues automáticos desde la rama principal.

Backend	en Render (Web Service):	Ejecución del servidor Node.js/Express. Se conecta de forma interna y segura con la base de datos, garantizando baja latencia.

Base de Datos	en Render (PostgreSQL):	Almacenamiento persistente y relacional de usuarios, obras y metadatos. Conectado al backend mediante Prisma ORM.

Almacenamiento	en Cloudinary (API):	Servicio externo especializado en el alojamiento y optimización de las imágenes protegidas (archivos binarios), liberando la carga de la base de datos principal.

## Equipo
Escobar Nuricumbo Heber Alexander-243691
Cuc López Axel Rodrigo-243702
Santillan Montesinos Eduardo-243747

## Docente: Viviana López Rojo