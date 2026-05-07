## ADDED Requirements

### Requirement: Música de fondo
El juego SHALL reproducir música de fondo tipo loop mientras el juego está activo, usando Web Audio API.

#### Scenario: Música durante el juego
- **WHEN** el usuario hace clic en "JUGAR"
- **THEN** la música de fondo SHALL comenzar a reproducirse en loop

#### Scenario: Música se detienen al morir
- **WHEN** el juego termina (Game Over)
- **THEN** la música de fondo SHALL detenerse

### Requirement: Sonido al comer zanahoria
El juego SHALL reproducir un efecto de sonido agradable cada vez que la serpiente come una zanahoria.

#### Scenario: Sonido al obtener puntuación
- **WHEN** la cabeza de la serpiente coincide con la posición de la zanahoria
- **THEN** SHALL reproducirse un sonido de "pickup" corto y agradable

### Requirement: Sonido al subir de nivel
El juego SHALL reproducir un sonido distintivo cada vez que el nivel aumenta.

#### Scenario: Sonido de nivel
- **WHEN** el puntaje alcanza un múltiplo de 100
- **THEN** SHALL reproducirse un sonido de "level up"

### Requirement: Sonido de Game Over
El juego SHALL reproducir un sonido cuando el jugador pierde.

#### Scenario: Sonido al morir
- **WHEN** la serpiente colisiona con un borde o consigo misma
- **THEN** SHALL reproducirse un sonido de "game over"