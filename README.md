<div align="center">

# 🤖 Asistente Académico Duoc UC 🇨🇱

[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=Streamlit&logoColor=white)](https://streamlit.io/)
[![LangChain](https://img.shields.io/badge/LangChain-121212?style=for-the-badge&logo=chainlink&logoColor=white)](https://python.langchain.com/)

Un asistente integral interactivo que utiliza la potencia de la **Inteligencia Artificial (RAG)** para la gestión y consulta de normativas institucionales. Desarrollado para ayudar a los estudiantes respondiendo de manera rápida, precisa y fundamentada, integrando además simuladores de carga académica y paneles de auditoría.

</div>

## 👨‍💻 Autor

Creado por **[Julio Andrés Contreras Olate]**

*   **GitHub:** [`@julcontrerasolate`](https://github.com/julcontrerasolate)

---

## 🎭 Módulos del Sistema

El asistente cuenta con tres módulos principales que puedes alternar en la plataforma para cubrir distintas necesidades académicas.

### 💬 Chatbot Documental (Reglamento)
*Tu compañero ideal para todo lo relacionado con las normativas de Duoc UC.* Te dará respuestas precisas, citará los artículos correspondientes y resolverá tus dudas sobre asistencia, notas y procesos. Utiliza un sistema RAG avanzado para evitar alucinaciones.

### 📅 Simulador de Toma de Ramos
*Gestión académica interactiva.* Un módulo que te permite filtrar asignaturas por carrera y semestre. Incluye un motor de validación lógica que detecta topes de horario y gestiona los cupos disponibles por sección en tiempo real.

### 🔐 Panel de Administración (Admin)
*Control total bajo la lupa.* Área exclusiva para coordinadores protegida por contraseña. Permite auditar el uso del bot, revisar métricas de satisfacción general (feedback de usuarios) y descargar registros detallados en formato `.csv` para análisis de datos.

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
