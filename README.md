# github-actions-lab

Este repositorio contiene un laboratorio práctico diseñado para implementar automatización de **Integración Continua y Despliegue Continuo (CI/CD)** utilizando **GitHub Actions**. 

El proyecto combina el código de una aplicación web estática con su infraestructura como código (IaC) gestionada por Terraform, permitiendo un flujo de trabajo completamente automatizado desde el commit hasta el despliegue final.

---

## ⚙️ Características del Laboratorio

* **Automatización con GitHub Actions**: Configuración de flujos de trabajo (*workflows*) automatizados para validar, estructurar y desplegar cambios en la infraestructura y la aplicación de manera desatendida.
* **Separación de Responsabilidades**: El repositorio separa claramente la lógica del código de la aplicación (`app`) de la definición de la infraestructura cloud (`infra`).
* **Infraestructura como Código (IaC)**: Despliegue de un sitio estático (*static site*) utilizando archivos de configuración de Terraform.

---

## 📁 Estructura del Proyecto

El repositorio se organiza en tres componentes esenciales:

* **`.github/workflows/`**: Aloja los pipelines de automatización de GitHub. Incluye el *workflow* de despliegue (`deploy workflow`) encargado de procesar la lógica de CI/CD.
* **`app/`**: Contiene los archivos fuente de la aplicación web (actualmente actualizada a su versión `v2`).
* **`infra/`**: Contiene los archivos de configuración de **Terraform** destinados a aprovisionar los recursos en la nube donde se hospeda el sitio web estático.

---

## 🔄 Flujo de Trabajo (CI/CD)

1. **Desarrollo**: Se realizan modificaciones en la aplicación (`app/`) o en la infraestructura (`infra/`).
2. **Validación Automática**: Al realizar un *push* o *pull request*, GitHub Actions ejecuta el pipeline para verificar la sintaxis (por ejemplo, corrección de indentaciones YAML o validaciones de Terraform).
3. **Despliegue**: El *workflow* se encarga de aplicar los cambios en la infraestructura y sincronizar la nueva versión de la aplicación de forma automática.
