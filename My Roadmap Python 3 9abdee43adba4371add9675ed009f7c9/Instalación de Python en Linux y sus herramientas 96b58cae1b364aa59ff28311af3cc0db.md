# Instalación de Python en Linux y sus herramientas

*Autor: Santiago I. Flores*

**Índice:**

⚠️ Falta agregar la instalación de: 🚨

- Conda, miniconda y anaconda
- Docker

******Contenidos:******

## **1. Preparación del Sistema**

Antes de instalar Python, asegurémonos de que tu sistema esté actualizado.

### **1.1. Revisar Actualizaciones:**

Verifica las actualizaciones disponibles.

```bash
sudo apt update
```

### **1.2. Aplicar Actualizaciones:**

Instala las actualizaciones identificadas.

```bash
sudo apt -y upgrade
```

- **Terminología Básica**:
    - **`sudo`**: Da permisos de administrador.
    - **`apt`**: Herramienta para gestionar paquetes.
    - **`update`**: Busca actualizaciones.
    - **`y`**: Acepta las operaciones propuestas.
    - **`upgrade`**: Instala las actualizaciones encontradas.

---

## **2. Instalación de Python**

Python es uno de los lenguajes de programación más populares. Veamos cómo instalarlo.

### **2.1. Instalar Python 3:**

```bash
sudo apt install -y python3
```

### **2.2. Verificar Instalación:**

Asegúrate de que Python esté instalado y verifica su versión.

```bash
python3 -V
```

- **Terminología Básica**:
    - **`install`**: Comando para añadir un programa.
    - **`python3`**: Versión de Python que estamos instalando.
    - **`V`**: Verifica la versión instalada.

---

## 3. ****Gestor de Herramientas Python (PIP3)****

### 3.1**. Instalar PIP3:**

Comando para instalar al administrador de herramientas Python, PIP3.

```bash
sudo apt install -y python3-pip
```

### 3.2**. Verificación de PIP3:**

Instrucción para validar la correcta implementación de PIP3.

```bash
pip3 -V
```

- **Terminología de Comandos:**
    - `install`: Directiva para añadir un paquete.
    - `python3-pip`: Administrador de herramientas de Python.
    - `V`: Comando para verificar la versión.

---

## 4. **Herramientas Esenciales de Desarrollo**

Comando para instalar las herramientas y bibliotecas esenciales que son comúnmente requeridas para compilar y construir software, especialmente aquellos relacionados con Python y aplicaciones que necesitan comunicaciones seguras o invocación de funciones entre lenguaje

```bash
sudo apt install -y build-essential libssl-dev libffi-dev python3-dev
```

- **Terminología de Comandos:**
    - `build-essential`: Es un paquete que instala muchas de las herramientas esenciales requeridas para compilar y construir software desde el código fuente en sistemas basados en Debian. Esto incluye cosas como el compilador GCC y herramientas relacionadas.
    - `libssl-dev`: Este paquete proporciona archivos de desarrollo para OpenSSL, que es una biblioteca de seguridad robusta que se utiliza para proporcionar comunicaciones seguras en redes y encriptación. Este paquete es necesario si planeas compilar software que requiera OpenSSL.
    - `libffi-dev`: Biblioteca de Invocación de Funciones Extranjeras (Foreign Function Interface, FFI) que proporciona una forma de llamar a funciones escritas en un lenguaje de programación desde otro. `libffi-dev` proporciona los archivos de desarrollo para esta biblioteca, y es comúnmente requerido para compilar ciertos paquetes de Python, como aquellos que requieren la extensión CFFI.
    - `python3-dev`: Contiene los archivos de encabezado y bibliotecas estáticas de Python que son necesarios si quieres compilar extensiones de Python o incrustar Python en otra aplicación.

---

## 5. **Entornos Virtuales**

Comando para instalar los entornos virtuales de Python.

```bash
sudo apt install -y python3-venv
```

---

## 6. **Herramienta: FastAPI**

### 6.1**. Instalación de FastAPI:**

Comando para instalar FastAPI, para desarrollo backend con Python.

```bash
pip3 install fastapi[all]
```

### 6.2**. Instalación de Uvicorn:**

Comando para instalar Uvicorn, permite ejecutar las aplicaciones creadas con FastAPI.

```bash
pip3 install uvicorn
```

---