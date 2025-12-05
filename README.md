# El Martillo OCR — Entrega de pipeline

Este proyecto documenta un pipeline de OCR para una página del periódico "El Martillo". Se intentaron tres enfoques (Google Vision API, Tesseract y EasyOCR) y se entregan los componentes clave: notebook, estructura de datos, CSV de salida y visualización.

## Estructura
- `notebooks/ocr_pipeline.ipynb`: notebook principal con intentos de OCR y fallback simulado.
- `data/el_martillo/page_01.png`: imagen de entrada.
- `data/processed/el_martillo_structured.csv`: salida estructurada.
- `requirements.txt`: dependencias usadas.

## Flujo
1. Intento de OCR con Google Vision (requiere credenciales).
2. Intento de OCR con Tesseract (si está instalado).
3. Intento de OCR con EasyOCR (dependencias puras de Python).
4. Si todo falla, se usa texto simulado para demostrar el pipeline.
5. Parseo, clasificación básica y exportación a CSV.
6. Visualización de distribución de tipos.

## Limitaciones y trabajo futuro
- Configurar correctamente credenciales de Google Vision.
- Instalar y validar `tesseract` y `traineddata` (spa/eng).
- Afinar reglas de parseo y mejorar la segmentación.
