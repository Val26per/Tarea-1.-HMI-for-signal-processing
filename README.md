Claro, aquí tienes la parte del `README.md` que se verá exactamente como deseas en GitHub — el bloque `bash` correctamente cerrado **y después el título como sección nueva**, igual a la **primera imagen** que mostraste:

```markdown
### Instalación de dependencias

Una vez activado el entorno virtual, instala las dependencias necesarias ejecutando:

```bash
pip install streamlit numpy matplotlib scipy soundfile pydub
```

Estas son las bibliotecas necesarias para ejecutar el proyecto:

- **streamlit**: Para construir la interfaz web interactiva.
- **numpy**: Para el manejo de arrays y cálculos numéricos.
- **matplotlib**: Para la visualización de señales.
- **scipy**: Para aplicar filtros digitales.
- **soundfile**: Para guardar los archivos de audio procesados.
- **pydub**: Para exportar audio en varios formatos (`.mp3`, `.aac`, `.wav`).

---

## 🧠 Estructura del Código

**Archivo principal:** `app.py`

| Función                         | Descripción                                                                 |
|--------------------------------|-----------------------------------------------------------------------------|
| `leer_audio_general(file)`     | Carga audio `.wav`, `.mp3`, `.aac` y lo convierte a array numpy mono        |
| `aplicar_filtro(...)`          | Aplica un filtro digital Butterworth con parámetros configurables           |
| `aplicar_fft(data, fs)`        | Calcula la FFT para visualizar el espectro de frecuencias                   |
| `st.line_chart()`              | Muestra la forma de onda del audio                                          |
| `st.pyplot()`                  | Muestra el espectro de frecuencias (FFT) con Matplotlib                     |
| `sf.write()`                   | Guarda el audio filtrado en un buffer WAV                                   |
| `AudioSegment.export()`        | Exporta el audio filtrado en `.mp3`, `.aac` o `.wav`                        |
```

✅ Este fragmento evitará que todo se encierre dentro del bloque `bash`, y al mismo tiempo mantendrá los títulos (`##`, `###`) con estilo bien visible.

¿Te lo dejo integrado a tu `README.md` completo actualizado?
