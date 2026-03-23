# Urban Grocers – Pruebas de API con pytest

Proyecto de automatización de pruebas de API para la funcionalidad de **creación de kits de productos** en la aplicación **Urban Grocers**, desarrollado como parte del Sprint 7 del Bootcamp de QA de TripleTen.

Valida que el endpoint de creación de kits responda correctamente ante distintos escenarios: datos válidos, límites de caracteres, campos vacíos y tipos de datos incorrectos.

---

## 🧪 Cobertura de pruebas

### Casos positivos
- Nombre con 1 carácter (límite inferior)
- Nombre con 511 caracteres (límite superior)
- Nombre con caracteres especiales
- Nombre con espacios

### Casos negativos
- Nombre vacío
- Nombre con 512 caracteres (fuera de límite)
- Nombre con tipo de dato incorrecto (número en lugar de string)
- Sin campo nombre en el body

---

## ⚙️ Tecnologías utilizadas

- **Lenguaje:** Python 3.x
- **Framework de pruebas:** pytest
- **Cliente HTTP:** requests
- **Patrón:** Separación en capas (configuración, datos, requests, tests)

---

## 🏗️ Estructura del proyecto

```
project/
│
├── configuration.py          ← URL base y endpoints
├── data.py                   ← Datos de prueba y body de requests
├── sender_stand_request.py   ← Funciones que llaman a la API
├── create_kit_name_kit_test.py ← Tests con pytest
└── README.md
```

---

## ▶️ Instalación y ejecución

```bash
# 1. Clonar el repositorio
git clone https://github.com/DavidHunter94/Proyecto-de-Pruebas-de-Creaci-n-de-Kits---Urban-Grocers.git
cd Proyecto-de-Pruebas-de-Creaci-n-de-Kits---Urban-Grocers

# 2. Instalar dependencias
pip install pytest requests

# 3. Ejecutar los tests
pytest -v
```

> ⚠️ Los tests requieren que el servidor de Urban Grocers esté activo.
> Esta URL es temporal del entorno de TripleTen y puede estar inactiva
> una vez finalizado el sprint.

---

## 🔍 Detalles de implementación

- **`configuration.py`** centraliza la URL base y los endpoints, facilitando cambios de entorno sin tocar los tests.
- **`data.py`** contiene todos los cuerpos de las requests, separando los datos de la lógica.
- **`sender_stand_request.py`** encapsula las llamadas HTTP, manteniendo los tests limpios y reutilizables.
- Los tests validan tanto el **status code** como el **contenido del body** de la respuesta.

---

## 🚀 Autor

**Victor David Martínez Matías**
QA Engineer con experiencia en pruebas manuales, automatización UI y pruebas de API. - Introducción a la automatización de pruebas
