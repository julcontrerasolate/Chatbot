<div align="center">

# 🤖 Asistente Académico Duoc UC 🇨🇱

[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=Streamlit&logoColor=white)](https://streamlit.io/)
[![LangChain](https://img.shields.io/badge/LangChain-121212?style=for-the-badge&logo=chainlink&logoColor=white)](https://python.langchain.com/)

Un asistente integral interactivo que utiliza la potencia de la **Inteligencia Artificial (RAG)** para la gestión y consulta de normativas institucionales. Desarrollado para ayudar a los estudiantes respondiendo de manera rápida, precisa y fundamentada, integrando además simuladores de carga académica y paneles de auditoría.

</div>

## 👨‍💻 Autor

Creado por **[Julio Andrés Contreras Olate]**

- **GitHub:** [`@julcontrerasolate`](https://github.com/julcontrerasolate)

---

## 🎭 Módulos del Sistema

El asistente cuenta con tres módulos principales que puedes alternar en la plataforma para cubrir distintas necesidades académicas.

## 🎥 Demostración del Asistente

<div align="center">
  <video src="video/Multimedia1.mp4" width="600" controls title="Demo Asistente Académico"></video>
</div>

### 💬 Chatbot Documental (Reglamento)

_Tu compañero ideal para todo lo relacionado con las normativas de Duoc UC._ Te dará respuestas precisas, citará los artículos correspondientes y resolverá tus dudas sobre asistencia, notas y procesos. Utiliza un sistema RAG avanzado para evitar alucinaciones.

### 📅 Simulador de Toma de Ramos

_Gestión académica interactiva._ Un módulo que te permite filtrar asignaturas por carrera y semestre. Incluye un motor de validación lógica que detecta topes de horario y gestiona los cupos disponibles por sección en tiempo real.

### 🔐 Panel de Administración (Admin)

_Control total bajo la lupa._ Área exclusiva para coordinadores protegida por contraseña. Permite auditar el uso del bot, revisar métricas de satisfacción general (feedback de usuarios) y descargar registros detallados en formato `.csv` para análisis de datos.

## 📂 Estructura del Proyecto

El proyecto está organizado de manera modular, separando la lógica de la interfaz, el procesamiento de documentos y la base de datos.

```text
chatbot-duoc-uc/
├── .streamlit/
│   └── secrets.toml       # Variables de entorno y credenciales (ignorado en git)
├── app.py                 # Archivo principal de ejecución (UI y lógica central)
├── reglamento.pdf         # Documento oficial para la ingesta de datos (RAG)
├── requirements.txt       # Dependencias y librerías del proyecto
├── styles.css             # Estilos globales personalizados
└── README.md              # Documentación del proyecto

```

## 🌟 Características

- **Interfaz Moderna:** Diseño bilingüe (Español/Inglés) con una UI limpia y responsiva construida con Streamlit y estilizada con CSS personalizado.
- **Recuperación Híbrida (Hybrid Search):** Implementación de `EnsembleRetriever`, combinando búsqueda semántica (30%) y búsqueda léxica con BM25 (70%) para máxima precisión.
- **Integración con IA Generativa:** Conectado a la API de **Groq (llama-3.1-8b-instant)** para generar respuestas ultrarrápidas, complementado con **Hugging Face** para embeddings locales.
- **Gestión de Base de Datos:** Uso de Supabase (PostgreSQL) para el registro de estudiantes, encriptación de contraseñas con `bcrypt` y almacenamiento del historial.

## 🛠️ Tecnologías Utilizadas

- **Lenguaje:** Python
- **Frontend:** Streamlit
- **Framework IA:** LangChain
- **LLM API:** Groq
- **Base de Datos:** Supabase

## 🌐 Despliegue en la Nube

Este proyecto está desplegado y funcionando de manera continua en **Streamlit Community Cloud**.

Las variables de entorno, como las claves de API de Groq y Supabase, están gestionadas de forma segura desde el panel de configuración (Secrets) de Streamlit, garantizando que ninguna credencial quede expuesta en el código fuente. Puedes probar la aplicación en vivo desde el botón en la parte superior de este documento.

## 🚀 Instalación y Ejecución Local

Si deseas probar o modificar el proyecto en tu propia máquina, sigue estos pasos:

### Prerrequisitos

- Python (v3.9 o superior)
- Git

### Pasos

1. **Clona el repositorio:**

```bash
git clone https://github.com/julcontrerasolate/Chatbot.git

```

2. **Navega a la carpeta del proyecto:**

```bash
cd Chatbot

```

3. **Crea y activa un entorno virtual:**

```bash
python -m venv venv
# En Windows (PowerShell):
.\venv\Scripts\Activate.ps1

```

4. **Instala las dependencias:**

```bash
pip install -r requirements.txt

```

5. **Configura las variables de entorno:**
   Crea una carpeta llamada `.streamlit` en la raíz del proyecto. Dentro, crea un archivo `secrets.toml` y añade tus claves:

```toml
GROQ_API_KEY="aqui_va_tu_api_key"
SUPABASE_URL="tu_url_de_supabase"
SUPABASE_KEY="tu_anon_key_de_supabase"
ADMIN_PASSWORD="DUOC2025"

```

6. **Ejecuta el servidor local:**

```bash
streamlit run app.py

```

Abre [http://localhost:8501](https://www.google.com/search?q=http://localhost:8501) en tu navegador para ver la aplicación funcionando.
