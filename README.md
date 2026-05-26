

<div align="center">

<img width="220" src="https://cdn-icons-png.flaticon.com/512/4712/4712109.png" />

# 🎙️ Whisper AI Speech Recognition

### Sistema avanzado de reconocimiento y transcripción de voz con IA 🚀

<p align="center">
  <b>Whisper</b> es un modelo de reconocimiento automático de voz desarrollado para transcribir audio, traducir idiomas y detectar lenguaje utilizando inteligencia artificial avanzada basada en Transformers.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/OpenAI-Whisper-412991?style=for-the-badge&logo=openai&logoColor=white">
  <img src="https://img.shields.io/badge/Python-AI-3776AB?style=for-the-badge&logo=python&logoColor=white">
  <img src="https://img.shields.io/badge/PyTorch-DeepLearning-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white">
  <img src="https://img.shields.io/badge/Transformer-SpeechRecognition-FF6F00?style=for-the-badge">
</p>

<p align="center">
  <a href="#-acerca-del-proyecto">Acerca</a> •
  <a href="#-características">Características</a> •
  <a href="#-modelos-disponibles">Modelos</a> •
  <a href="#-instalación">Instalación</a> •
  <a href="#-uso">Uso</a>
</p>

</div>

---

# 🌌 Acerca del proyecto

**Whisper AI Speech Recognition** es un sistema de reconocimiento de voz basado en inteligencia artificial capaz de:

- 🎤 Transcribir audio automáticamente
- 🌍 Detectar múltiples idiomas
- 🔄 Traducir voz a inglés
- 🧠 Procesar lenguaje natural
- 📡 Analizar audio en tiempo real
- ⚡ Ejecutar inferencias con modelos Transformer
- 🗣️ Reconocer voz multilenguaje
- 🤖 Integrarse con aplicaciones de IA

El modelo fue entrenado utilizando enormes cantidades de datos de audio y lenguaje para ofrecer resultados precisos y robustos.

---

# ✨ Características

## 🎙️ Reconocimiento de voz

- 📢 Transcripción automática
- 🌐 Soporte multilenguaje
- ⚡ Alta precisión
- 🧠 IA basada en Transformers
- 🔊 Procesamiento de audio avanzado

---

## 🌍 Traducción y detección de idiomas

- 🇯🇵 Japonés
- 🇪🇸 Español
- 🇺🇸 Inglés
- 🇫🇷 Francés
- 🇩🇪 Alemán
- 🌎 Más de 90 idiomas compatibles

---

## ⚙️ Inteligencia artificial

- 🤖 Deep Learning
- 🧠 Modelos Transformer
- 🔍 Detección automática de idioma
- 📊 Procesamiento de secuencias
- 🚀 Optimización GPU

---

## 🔥 Rendimiento avanzado

- ⚡ Procesamiento rápido
- 💾 Diferentes tamaños de modelo
- 🎯 Balance entre velocidad y precisión
- 📈 Escalable para producción
- 🔄 Compatible con CPU y GPU

---

# 🧠 Arquitectura del sistema

## ⚙️ Pipeline de procesamiento

1️⃣ Carga del archivo de audio  
2️⃣ Conversión a espectrograma Mel  
3️⃣ Procesamiento con Transformer  
4️⃣ Detección de idioma  
5️⃣ Decodificación de voz  
6️⃣ Generación del texto final  

---

# 📊 Modelos disponibles

| Modelo | Parámetros | VRAM Aproximada | Velocidad |
|--------|-------------|----------------|------------|
| Tiny | 39M | ~1 GB | ~32x |
| Base | 74M | ~1 GB | ~16x |
| Small | 244M | ~2 GB | ~6x |
| Medium | 769M | ~5 GB | ~2x |
| Large | 1550M | ~10 GB | ~1x |

---

# 🛠️ Tecnologías utilizadas

## 🧠 Inteligencia Artificial

<p>
  <img src="https://skillicons.dev/icons?i=python,pytorch" />
</p>

- Python
- PyTorch
- Transformers
- Deep Learning
- Machine Learning

---

## 🔊 Procesamiento de audio

<p>
  <img src="https://skillicons.dev/icons?i=linux" />
</p>

- FFmpeg
- Audio Processing
- Mel Spectrograms
- Speech Recognition
- Voice Detection

---

## 🧰 Herramientas

<p>
  <img src="https://skillicons.dev/icons?i=git,github,vscode" />
</p>

- Git
- GitHub
- VS Code
- Jupyter Notebook
- Python Pip

---

# 📂 Estructura del proyecto

```bash
WhisperAI/
│
├── whisper/                 # Código principal del modelo
├── notebooks/               # Ejemplos en Jupyter
├── audio_samples/           # Archivos de prueba
├── models/                  # Modelos descargados
├── scripts/                 # Scripts auxiliares
├── tests/                   # Pruebas
├── requirements.txt
├── setup.py
├── LICENSE
└── README.md
```

---

# ⚡ Instalación

## 📋 Requisitos

- Python 3.7+
- Pip
- FFmpeg
- GPU opcional (CUDA)
- PyTorch

---

# 🚀 Configuración del proyecto

## 1️⃣ Clonar repositorio

```bash
git clone https://github.com/openai/whisper.git
```

---

## 2️⃣ Entrar al proyecto

```bash
cd whisper
```

---

## 3️⃣ Instalar dependencias

```bash
pip install git+https://github.com/openai/whisper.git
```

---

## 4️⃣ Instalar FFmpeg

### Ubuntu / Debian

```bash
sudo apt update && sudo apt install ffmpeg
```

### Arch Linux

```bash
sudo pacman -S ffmpeg
```

### MacOS

```bash
brew install ffmpeg
```

### Windows (Chocolatey)

```bash
choco install ffmpeg
```

---

# 🎤 Uso desde terminal

## Transcribir audio

```bash
whisper audio.mp3
```

---

## Usar modelo específico

```bash
whisper audio.mp3 --model medium
```

---

## Traducir audio

```bash
whisper japanese.wav --language Japanese --task translate
```

---

## Mostrar ayuda

```bash
whisper --help
```

---

# 🐍 Uso con Python

## Ejemplo básico

```python
import whisper

model = whisper.load_model("base")

result = model.transcribe("audio.mp3")

print(result["text"])
```

---

## Detectar idioma

```python
import whisper

model = whisper.load_model("base")

audio = whisper.load_audio("audio.mp3")
audio = whisper.pad_or_trim(audio)

mel = whisper.log_mel_spectrogram(audio).to(model.device)

_, probs = model.detect_language(mel)

print(max(probs, key=probs.get))
```

---

# 📈 Funcionalidades principales

## 🎙️ Speech Recognition

- Reconocimiento automático
- Transcripción precisa
- Procesamiento de voz
- Detección de lenguaje

---

## 🌍 Traducción

- Traducción automática
- Conversión multilenguaje
- Interpretación de voz

---

## ⚡ IA y Deep Learning

- Transformers
- Redes neuronales
- NLP
- Machine Learning

---

# 🧪 Aplicaciones

## 🚀 Casos de uso

- Subtítulos automáticos
- Asistentes virtuales
- Traducción en tiempo real
- Chatbots con voz
- Sistemas de accesibilidad
- Transcripción de reuniones
- Automatización empresarial

---

# 🧠 Objetivos del proyecto

## 🎯 Aprendizaje y desarrollo

- Inteligencia Artificial
- Speech Recognition
- Deep Learning
- Transformers
- NLP
- Procesamiento de audio
- Machine Learning

---

# 🚧 Roadmap

## 🔮 Próximas mejoras

- ⚡ Inferencia más rápida
- 🌐 Más idiomas
- 📱 Integración móvil
- 🤖 Mejoras de IA
- 🔊 Audio en tiempo real
- ☁️ Deploy cloud
- 🎧 Streaming de audio

---

# 🤝 Contribuciones

Las contribuciones son bienvenidas ❤️

## Cómo contribuir

1. Fork del proyecto

```bash
git checkout -b feature/nueva-funcionalidad
```

2. Commit

```bash
git commit -m "✨ Nueva funcionalidad"
```

3. Push

```bash
git push origin feature/nueva-funcionalidad
```

4. Pull Request 🚀

---

# 👨‍💻 Desarrollador

<div align="center">

## OpenAI — Artificial Intelligence Research

Proyecto enfocado en reconocimiento de voz, inteligencia artificial y procesamiento avanzado de lenguaje natural 🚀

</div>

---

# 🌟 Apoya el proyecto

⭐ Dale una estrella  
🍴 Haz fork  
📢 Comparte el proyecto  

---

# 📜 Licencia

Proyecto open source bajo licencia MIT orientado al desarrollo de sistemas de reconocimiento de voz e inteligencia artificial.

---

<div align="center">

### 🎙️ Whisper AI Speech Recognition — inteligencia artificial avanzada para voz y lenguaje 🚀

</div>
