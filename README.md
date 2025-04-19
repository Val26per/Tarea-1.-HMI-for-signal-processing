# 🎚️ Procesamiento de Audio con Filtros Digitales

**Interfaces de Hardware y Software — Proyecto de Interfaz HMI en Streamlit**

---

## 📄 Descripción

Este proyecto implementa un sistema de **procesamiento de señales de audio** mediante filtros digitales (pasa bajas, pasa altas y pasa banda).  
La interfaz gráfica fue desarrollada con **Streamlit** y permite:

- Cargar archivos de audio `.wav`, `.mp3`, `.aac`
- Aplicar filtros digitales configurables
- Visualizar el audio en el **dominio del tiempo** y en el **dominio de la frecuencia (FFT)**
- Exportar el resultado en diferentes formatos

---

## ⚙️ Requisitos

- Python 3.10 instalado

### Instalación de dependencias:

```bash
pip install streamlit numpy matplotlib scipy soundfile pydub
## 🧠 Estructura del Código

**Archivo principal:** `app.py`

| Función | Descripción |
|--------|-------------|
| `leer_audio_general(file)` | Carga audio `.wav`, `.mp3`, `.aac` y lo convierte a array numpy mono |
| `aplicar_filtro(data, fs, tipo, fc_low, fc_high, orden)` | Aplica filtro digital Butterworth según los parámetros definidos |
| `aplicar_fft(data, fs)` | Calcula la FFT para visualizar el espectro de frecuencias |
| `st.line_chart()` | Muestra la forma de onda del audio |
| `st.pyplot()` | Muestra el espectro de frecuencias (FFT) con Matplotlib |
| `sf.write()` | Guarda el audio filtrado en un buffer |
| `AudioSegment.export()` | Exporta el audio filtrado en formato `.mp3`, `.aac` o `.wav` |

---

## 🧪 Instrucciones de Uso

### Paso 1️⃣: Cargar audio

- Selecciona un archivo de audio en formato `.wav`, `.mp3`, o `.aac`.
- Se mostrará la forma de onda del audio cargado en un gráfico interactivo.

---

### Paso 2️⃣: Aplicar filtro

1. Elige el tipo de filtro:
   - `Pasa-bajas`
   - `Pasa-altas`
   - `Pasa-banda`
2. Ajusta los parámetros del filtro:
   - **Orden del filtro**
   - **Frecuencia(s) de corte**
3. Haz clic en **Aplicar filtro** para procesar la señal.

---

### 🔉 Visualización de Audio Filtrado

- Se reproducen tanto el audio **original** como el **filtrado**.
- Se visualizan ambas formas de onda para comparar resultados antes y después del filtrado.

---

### Paso 3️⃣: Transformada de Fourier (FFT)

- Presiona el botón **Aplicar FFT**.
- Se mostrarán los espectros de frecuencia del audio original y del filtrado para su comparación.

---

### 💾 Guardar Resultado

- Selecciona el formato de exportación deseado: `.wav`, `.mp3` o `.aac`.
- Haz clic en el botón **Guardar Resultado**.
- Luego, presiona **⬇️ Descargar archivo** para obtener el audio procesado.

---

## 🚀 Ejecutar la Aplicación

Para correr la aplicación, abre una terminal en el directorio del proyecto y ejecuta:

```bash
streamlit run app.py
