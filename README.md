# 🎧 HMI para Procesamiento de Señales de Audio (con Streamlit)

## 📌 Trabajo 1 - Interfaces de Hardware y Software

Este proyecto implementa una **interfaz humano-máquina (HMI)** para el procesamiento digital de señales de audio usando Streamlit. El usuario puede cargar un archivo de audio, aplicar filtros digitales, visualizar la señal en el dominio del tiempo y la frecuencia (FFT), y descargar el audio filtrado.

---

## 📄 Descripción

La aplicación permite:

- Cargar archivos `.wav`, `.mp3` o `.aac`.
- Aplicar filtros:
  - Pasa-bajas
  - Pasa-altas
  - Pasa-banda
- Visualizar señales:
  - Forma de onda (dominio del tiempo)
  - Espectro de frecuencia (FFT)
- Escuchar audio original y filtrado.
- Descargar el audio procesado en `.wav`, `.mp3` o `.aac`.

---

## ⚙️ Requisitos

- Python 3.10
- pip

### 📦 Instalación de dependencias

```bash
pip install streamlit numpy matplotlib scipy pydub soundfile
