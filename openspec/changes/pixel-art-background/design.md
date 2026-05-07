## Context

El juego Snake actual tiene un fondo oscuro sólido (#0f0f23). Se necesita agregar carga de imagen y convertirla a pixel art para usarla como fondo.

## Goals / Non-Goals

**Goals:**
- Input file para subir imágenes PNG/JPEG/JPG
- Convertir imagen a pixel art del tamaño de la cuadrícula (30x30)
- Dibujar el pixel art como fondo del canvas
- Cachear el resultado para no reprocesar cada frame

**Non-Goals:**
- Edición de la imagen
- Soportar GIF o video
- Filtros adicionales

## Decisions

- **Canvas API**: Usar `drawImage` + `getImageData` para reducir la imagen a 30x30 píxeles (pixel art)
- **ImageData**: Escalar cada píxel a 20x20 (GRID_SIZE) para el fondo final
- **Input file oculto**: Botón personalizado para mejor UX

## Risks / Trade-offs

- [Riesgo: imagen muy grande] → [Mitigación: redimensionar antes de procesar]
- [Riesgo: CORS en imagen local] → [Mitigación: FileReader + URL.createObjectURL]
