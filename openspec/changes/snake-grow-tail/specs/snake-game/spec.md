## MODIFIED Requirements

### Requirement: Sistema de puntuación
El juego SHALL otorgar 10 puntos cada vez que la serpiente alcanza una zanahoria, Y la serpiente SHALL crecer un segmento.

#### Scenario: Obtener puntuación y crecer
- **WHEN** la cabeza de la serpiente coincide con la posición de la zanahoria
- **THEN** el puntaje SHALL aumentar en 10 puntos Y la serpiente SHALL agregar un nuevo segmento a su cuerpo