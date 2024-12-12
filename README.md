# iac

Este repositorio está diseñado para ser gestionado mediante **argocd-autopilot** y para administrar configuraciones de **argocd-autopilot como código**, permitiendo la automatización y versionado de la infraestructura.

---

## Propósito

El objetivo principal de este repositorio es:
- Centralizar las configuraciones y recursos gestionados por **argocd-autopilot**.
- Versionar las definiciones de aplicaciones, recursos y proyectos de manera declarativa.
- Automatizar la administración de ArgoCD en entornos Kubernetes.

---

## Estructura del Repositorio

### **`apps/`**
Contiene las configuraciones de aplicaciones organizadas por entorno y caso de uso:
- **`demo/`**, **`opentwins/`**, **`telefonica/`**: Agrupaciones de configuraciones para entornos `digital-twins`, `edge`, `region` y `wavelength`.
- `config_dir.json`: Archivos de configuración que definen parámetros específicos para cada entorno.

### **`bootstrap/`**
Archivos necesarios para inicializar y configurar el entorno de ArgoCD y sus recursos:
- **`argo-cd/`**: Configuraciones específicas de ArgoCD como `ingress.yaml` y `kustomization.yaml`.
- **`cluster-resources/`**: Recursos iniciales del clúster, como espacios de nombres para ArgoCD.

### **`projects/`**
Define proyectos y configuraciones generales, como:
- `addons.yaml`: Complementos adicionales.
- `clusters.yaml`: Definición de clústeres.
- `digital-twins.yaml`: Configuraciones específicas de gemelos digitales.

---

## Notas

- Este repositorio es autogestionado a través de los pipelines CICD

