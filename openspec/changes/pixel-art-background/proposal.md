## Why

Personalizar el fondo del canvas del juego Snake convirtiendo una imagen subida por el usuario en pixel art. Esto permite que cada jugador tenga un fondo único y personalizado.

## What Changes

- Input para que el usuario cargue una imagen (PNG, JPEG, JPG)
- Convertir la imagen a pixel art y usarla como fondo del canvas
- La imagen se redimensiona a la cuadrícula del juego (30x30 tiles)
- Mantener el rendimiento del juego

## Capabilities

### New Capabilities
- **image-to-pixelart**: Sistema para cargar imagen y convertirla a pixel art como fondo del canvas

### Modified Capabilities
- (ninguno)

## Impact

- Modificar archivo: `index.html`
- Agregar input de tipo file en HTML
- Agregar lógica JavaScript para procesar imagen con Canvas API
- Sin dependencias externas
