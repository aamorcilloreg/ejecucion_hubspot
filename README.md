# Ejecución Periódica de Notebook para HubSpot

Este repositorio contiene un notebook de Python diseñado para realizar cargas de datos o actualizaciones en HubSpot. El proyecto está configurado para ser ejecutado de forma automática y periódica utilizando GitHub Actions.

---

## 📋 Contenido del Repositorio

* **`Actualizar_celular_Hubspot.ipynb`**: El notebook principal que contiene toda la lógica para conectarse a las APIs, procesar los datos y actualizar los contactos en HubSpot.
* **`.github/workflows/main.yml`**: El archivo de configuración de GitHub Actions que define el calendario y los pasos para la ejecución automática del notebook.
* **`requirements.txt`**: Un listado de todas las librerías de Python necesarias para que el notebook funcione correctamente.

---

## ⚙️ Configuración y Uso

Para que este proyecto funcione, se requiere una configuración previa.

### 1. Manejo de Secretos

La API Key de HubSpot es un dato sensible y **no está guardada en el código**. En su lugar, se almacena de forma segura en los "Secrets" de GitHub.

* Para configurar la llave, ve a `Settings` > `Secrets and variables` > `Actions` y crea un nuevo "repository secret" con el nombre `HUBSPOT_API_KEY`.

### 2. Ejecución

El notebook se ejecuta a través de un workflow de GitHub Actions definido en el archivo `main.yml`.

* **Ejecución Manual**: Puedes disparar el proceso manualmente en cualquier momento. Ve a la pestaña `Actions`, selecciona el workflow **"Ejecutar Notebook de HubSpot"** y haz clic en **"Run workflow"**.
* **Ejecución Calendarizada**: La ejecución automática está configurada pero actualmente desactivada. Para activarla, edita el archivo `.github/workflows/main.yml` y descomenta (borra los `#`) las siguientes líneas:
    ```yaml
    # on:
    #   schedule:
    #     - cron: '0 17 * * *'
    ```

---
_Este README fue generado con la ayuda de un asistente de IA._
