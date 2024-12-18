# **Gestor de Despliegues con GitOps: Hola Mundo**

Este repositorio contiene los archivos necesarios para desplegar una aplicación simple que muestra el mensaje **"Hola Mundo"** utilizando **GitOps** con Kubernetes y ArgoCD.

---

## **Descripción del Proyecto**
Esta aplicación es un sitio web básico empaquetado en una imagen Docker y desplegado en Kubernetes. El flujo GitOps asegura que cualquier cambio en los archivos de configuración almacenados en este repositorio se sincronice automáticamente con el clúster.

---

## **Estructura del Repositorio**
```plaintext
my-gitops-hola-mundo/
├── deployment.yaml   # Configuración del despliegue en Kubernetes
├── service.yaml      # Configuración del servicio para exponer la aplicación
├── index.html        # Archivo HTML simple con el mensaje "Hola Mundo"
├── Dockerfile        # Archivo Docker para empaquetar la aplicación
└── README.md         # Documentación del proyecto
