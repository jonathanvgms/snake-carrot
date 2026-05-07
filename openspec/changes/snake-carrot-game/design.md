## Context

Juego Snake clásico en un solo archivo HTML con CSS y JavaScript embebido. El jugador controla una serpiente que debe perseguir zanahorias para obtener puntos. Cada 100 puntos, el nivel aumenta y la velocidad del juego incrementa.

## Goals / Non-Goals

**Goals:**
- Crear un juego funcional con mecánicas de Snake clásico
- Sistema de puntuación: 10 puntos por zanahoria
- Niveles que aumentan la velocidad del juego
- Interfaz visual atractiva

**Non-Goals:**
- Modo multiplayer
- Guardado de puntuación en servidor
- Efectos de sonido

## Decisions

- **Canvas HTML5**: Usar `<canvas>` para renderizar el juego por rendimiento
- **Grid-based movement**: Movimiento en incrementos de cuadrícula (no continuo)
- **requestAnimationFrame/setInterval**: Usar setInterval para control de velocidad

## Risks / Trade-offs

- [Riesgo: velocidad variable en diferentes navegadores] → [Mitigación: usar setInterval con tiempo fijo]
- [Riesgo: la comida aparece en la serpiente] → [Mitigación: validar posición antes de colocar comida]