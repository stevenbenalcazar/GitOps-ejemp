Gestor de Despliegues con GitOps: Hola Mundo
Este repositorio contiene los archivos necesarios para desplegar una aplicación simple que muestra el mensaje "Hola Mundo" utilizando GitOps con Kubernetes y ArgoCD.

Descripción del Proyecto
La aplicación es un sitio web básico empaquetado en una imagen Docker y desplegado en Kubernetes. El flujo GitOps garantiza que cualquier cambio en los archivos de configuración almacenados en este repositorio se sincronice automáticamente con el clúster.

Estructura del Repositorio
plaintext
Copiar código
my-gitops-hola-mundo/
├── deployment.yaml   # Configuración del despliegue de Kubernetes
├── service.yaml      # Configuración del servicio para exponer la aplicación
└── README.md         # Documentación del proyecto
Requisitos Previos
Un clúster de Kubernetes configurado.
ArgoCD instalado y funcionando en el clúster.
Acceso a Docker y un registro de imágenes (Docker Hub, etc.).
Kubectl configurado para interactuar con el clúster.
Pasos para Implementar
1. Construcción de la Aplicación
Crea y sube la imagen Docker para la aplicación:

bash
Copiar código
docker build -t tuusuario/hola-mundo:v1 .
docker push tuusuario/hola-mundo:v1
2. Configuración de Kubernetes
Asegúrate de que ArgoCD está instalado en tu clúster.
Aplica los siguientes archivos de configuración al clúster (ArgoCD los sincronizará automáticamente si está configurado):
deployment.yaml: Define el despliegue de la aplicación.
service.yaml: Configura el servicio para exponer la aplicación.
3. Configuración de ArgoCD
Accede al panel de ArgoCD.

Crea una aplicación vinculada a este repositorio:

Repositorio Git: URL de este repositorio.
Ruta: Directorio raíz (donde están los archivos YAML).
Destino: Tu clúster y namespace (default)
