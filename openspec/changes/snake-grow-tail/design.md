## Context

El juego Snake existente ya tiene un sistema de puntuación donde la serpiente no crece al comer zanahorias. El código actual tiene una condición donde cuando come una zanahoria, NO hace pop() (no elimina la cola), lo cual teóricamente debería hacer crecer la serpiente. Pero revisando el código anterior, parece que la serpiente sí crece correctamente - el segmento de la cabeza se agrega y solo se elimina el último segmento si NO come zanahoria.

## Goals / Non-Goals

**Goals:**
- Verificar que la serpiente crece correctamente al comer zanahorias
- Asegurar que el crecimiento sea visible y fluido

**Non-Goals:**
- Limitar el crecimiento máximo
- Agregar efectos visuales adicionales

## Decisions

- El código actual YA implementa crecimiento: cuando come zanahoria, no se hace pop(), agregando un segmento nuevo

## Risks / Trade-offs

- [Riesgo: performance con serpiente muy larga] → [Mitigación: grid pequeño, no debería ser problema]
- [Riesgo: la lógica actual no funciona] → [Verificar y corregir si es necesario]