Práctica de Entrega Continua – Hola Mundo DevOps

Descripción del proyecto

Este proyecto consiste en automatizar el proceso de construcción, publicación y despliegue de una aplicación web sencilla utilizando Docker, Docker Hub, GitHub Actions y Render.

El objetivo es implementar un flujo de Integración y Entrega Continua (CI/CD) que permita publicar automáticamente los cambios realizados en el repositorio.

Tecnologías utilizadas

HTML: estructura de la aplicación web.

Docker: creación de la imagen de la aplicación.

Docker Hub: almacenamiento y publicación de la imagen.

GitHub: alojamiento del código fuente.

GitHub Actions: automatización del proceso CI/CD.

Render: despliegue de la aplicación en producción.

Nginx: servidor web utilizado dentro del contenedor.

Estructura del proyecto

Practica-Entrega-Continua/
│
├── .github/
│   └── workflows/
│       └── docker-publish.yml
│
├── Dockerfile
├── index.html
└── README.md

Funcionamiento de la automatización

El flujo de trabajo se ejecuta cuando se realizan cambios y se envían a la rama main del repositorio.

El proceso realiza los siguientes pasos:

Descarga el código del repositorio mediante GitHub Actions.

Inicia sesión en Docker Hub utilizando los secretos configurados en GitHub.

Construye la imagen Docker utilizando el Dockerfile.

Publica la imagen en Docker Hub con las etiquetas latest y 1.0.

Ejecuta el Deploy Hook de Render para iniciar el despliegue de la aplicación.

También se puede ejecutar manualmente desde la pestaña Actions de GitHub.

Enlaces del proyecto

Recurso

Enlace

Repositorio GitHub

https://github.com/Jatna-19/Practica-Entrega-Continua

Aplicación en producción

https://hola-mundo-devops-ppi1.onrender.com

Imagen en Docker Hub

https://hub.docker.com/r/jatna/hola-mundo-devops

Ejecución local con Docker

Para ejecutar la aplicación localmente, primero se debe clonar el repositorio:

git clone https://github.com/Jatna-19/Practica-Entrega-Continua.git

Entrar a la carpeta del proyecto:

cd Practica-Entrega-Continua

Construir la imagen:

docker build -t hola-mundo-devops .

Ejecutar el contenedor:

docker run -d -p 8080:80 --name hola-mundo hola-mundo-devops

Abrir en el navegador:

http://localhost:8080

Seguridad

Las credenciales de Docker Hub y el enlace de despliegue de Render se almacenan en GitHub Secrets para evitar que se publiquen directamente en el código del repositorio.

Los secretos utilizados son:

DOCKERHUB_USERNAME

DOCKERHUB_TOKEN_NUEVO

RENDER_DEPLOY_HOOK_URL

No se deben compartir los valores de estos secretos.

Resultado obtenido

Se implementó un flujo automatizado que permite construir y publicar la imagen de Docker en Docker Hub y activar el despliegue de la aplicación en Render mediante GitHub Actions.

La aplicación se encuentra disponible públicamente y puede consultarse desde el enlace de producción.

Autor

Jatna Massiel De La Cruz Mejía

Instituto Tecnológico de Las Américas (ITLA)

Tecnólogo en Desarrollo de Software
