## Context

El juego Snake actual no tiene ningún tipo de audio. Se usará Web Audio API nativa del navegador para generar sonidos sin necesidad de archivos externos.

## Goals / Non-Goals

**Goals:**
- Música de fondo tipo loop durante el juego
- Efecto de sonido al comer zanahoria
- Efecto de sonido al subir de nivel
- Efecto de sonido en Game Over

**Non-Goals:**
- Sonidos para movimiento de la serpiente
- Configuración de volumen
- Guardar preferencias de audio

## Decisions

- **Web Audio API**: Usar la API nativa del navegador para generar sonidos sintetizados
- **Osciladores**: Usar osciladores para crear tonos simples (no samples)
- **Música procedural**: Crear melodía simple con secuencia de notas

## Risks / Trade-offs

- [Riesgo: navegador sin soporte Web Audio] → [Mitigación: verificar disponibilidad antes de usar]
- [Riesgo: audio no funciona hasta primera interacción] → [Mitigación: iniciar audio al hacer click en "JUGAR"]
- [Riesgo: sonidos muy simples] → [Mitigación: usar combinación de osciladores para mejor sonido]
