# Práctica de Entrega Continua – Hola Mundo DevOps

## 1. Descripción del proyecto

Este proyecto consiste en implementar un proceso de Integración y Entrega Continua (CI/CD) para una aplicación web sencilla utilizando Docker, Docker Hub, GitHub Actions y Render.

El objetivo es automatizar la construcción de la imagen Docker, su publicación en Docker Hub y el despliegue de la aplicación en un entorno de producción.

## 2. Tecnologías utilizadas

- **HTML:** estructura de la aplicación web.
- **Docker:** creación y ejecución de contenedores.
- **Docker Hub:** almacenamiento y publicación de imágenes Docker.
- **GitHub:** alojamiento del código fuente.
- **GitHub Actions:** automatización del flujo de trabajo.
- **Render:** alojamiento y despliegue de la aplicación.
- **Nginx:** servidor web utilizado para ejecutar la aplicación.

## 3. Estructura del proyecto

```text
Practica-Entrega-Continua/
│
├── .github/
│   └── workflows/
│       └── docker-publish.yml
│
├── Dockerfile
├── index.html
└── README.md
