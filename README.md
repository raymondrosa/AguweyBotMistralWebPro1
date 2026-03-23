AguweyBot 🤖
Asistente inteligente con Ministral-3 para análisis de documentos y conversaciones con audio

📋 Descripción
AguweyBot es un asistente virtual basado en el modelo Ministral-3 de Mistral AI, diseñado para el análisis profundo de documentos y conversaciones interactivas. Cuenta con capacidades de lectura de múltiples formatos, generación de audio a partir de respuestas y una interfaz moderna con efectos visuales.

✨ Características principales
📄 Soporte multi-formato: PDF, Excel (XLSX/XLS), CSV, TXT, Word (DOCX)

🎯 Análisis completo: Lee el contenido total de los archivos para responder preguntas

🔊 Texto a voz: Conversión de respuestas a audio con gTTS

📋 Copiado rápido: Botón integrado para copiar respuestas

🎨 Interfaz visual: Diseño con efectos neon, blur, gradientes y animaciones

⚡ Streaming en tiempo real: Respuestas generadas con efecto de escritura

📊 Estadísticas de conversación: Visualización de métricas en sidebar

🔄 Gestión de contexto: Manejo inteligente del historial de mensajes

🚀 Demo en vivo
Puedes probar la aplicación en: https://aguweybot.streamlit.app

🛠️ Tecnologías utilizadas
Tecnología	Uso
Streamlit	Framework para la interfaz web
Mistral AI API	Modelo de lenguaje (ministral-3b-latest)
PyPDF2	Extracción de texto de PDFs
python-docx	Lectura de documentos Word
pandas	Manejo de datos CSV/Excel
gTTS	Conversión texto a voz (Google Text-to-Speech)
chardet	Detección de codificaciones
Pillow	Manejo de imágenes
📁 Estructura del proyecto
text
aguweybot/
├── aguweybotweb.py          # Archivo principal de la aplicación
├── requirements.txt         # Dependencias del proyecto
├── .streamlit/
│   └── secrets.toml         # Configuración de API keys (no subir al repo)
├── logo.png                 # Logo de la aplicación (opcional)
├── fondo.png                # Imagen de fondo (opcional)
└── README.md                # Este archivo
🔧 Instalación local
Prerrequisitos
Python 3.9 o superior

API Key de Mistral AI

Pasos
Clonar el repositorio

bash
git clone https://github.com/tu-usuario/aguweybot.git
cd aguweybot
Crear entorno virtual

bash
python -m venv venv
source venv/bin/activate  # En Windows: venv\Scripts\activate
Instalar dependencias

bash
pip install -r requirements.txt
Configurar API Key

Crea el archivo .streamlit/secrets.toml:

toml
MISTRAL_API_KEY = "tu-api-key-aqui"
Ejecutar la aplicación

bash
streamlit run aguweybotweb.py
☁️ Despliegue en Streamlit Cloud
Sube el código a un repositorio de GitHub

Ve a share.streamlit.io y conecta tu repositorio

Configura los secrets en Streamlit Cloud:

Ve a Settings > Secrets

Agrega: MISTRAL_API_KEY = "tu-api-key"

Asegúrate de que requirements.txt incluya:

text
streamlit>=1.28.0
mistralai>=1.0.0
PyPDF2>=3.0.0
python-docx>=1.1.0
pandas>=2.0.0
gtts>=2.3.0
chardet>=5.0.0
Pillow>=10.0.0
Haz clic en Deploy y espera a que termine el despliegue

📖 Uso de la aplicación
Cargar un archivo
En el panel izquierdo, haz clic en "Subir Archivo"

Selecciona un archivo (PDF, Excel, CSV, TXT, DOCX)

Haz clic en "Leer TODO" para procesarlo

Realizar preguntas
Una vez cargado el archivo, escribe tu pregunta en el chat

El asistente analizará el contenido completo del archivo

Puedes pedir resúmenes, análisis de datos, explicaciones de código, etc.

Funciones adicionales
🔊 Escuchar: Convierte cualquier respuesta a audio

📋 Copiar: Copia el texto de una respuesta al portapapeles

🔄 Nueva Conversación: Reinicia el historial de mensajes

⚙️ Configuración avanzada
Puedes modificar las siguientes constantes en el archivo aguweybotweb.py:

python
class Config:
    PRIMARY_COLOR = "#00ffff"           # Color principal
    MAX_HISTORY_MESSAGES = 10           # Mensajes de contexto
    MAX_FILE_SIZE_MB = 50               # Límite de archivos (MB)
    MAX_CONTEXT_TOKENS = 8000           # Tokens máximos para contexto
📝 Notas importantes
Límite de contexto: Ministral-3 tiene un límite de 8000 tokens. Los archivos muy grandes se truncan automáticamente.

Audio: La generación de audio utiliza gTTS, que requiere conexión a internet.

PDFs: Solo se extrae texto de PDFs con capa de texto (no escaneados).

👨‍💻 Autor
Prof. Raymond Rosa Ávila

📧 raymondrosaavila@gmail.com

🔗 GitHub

📄 Licencia
Este proyecto está bajo la licencia Creative Commons Attribution-ShareAlike (CC-SA).

Puedes:

✅ Compartir — copiar y redistribuir el material en cualquier medio o formato

✅ Adaptar — remezclar, transformar y construir a partir del material

Bajo las siguientes condiciones:

📌 Atribución — Debes dar crédito adecuado

🔗 CompartirIgual — Si remezclas, transformas o creas a partir del material, debes distribuir tus contribuciones bajo la misma licencia

🙏 Agradecimientos
Mistral AI por proporcionar el modelo Ministral-3

Streamlit por el increíble framework

Comunidad open-source por las bibliotecas utilizadas

⭐ Si te gusta este proyecto, no olvides darle una estrella en GitHub ⭐
