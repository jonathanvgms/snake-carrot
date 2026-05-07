## ADDED Requirements

### Requirement: Movimiento de la serpiente
La serpiente SHALL moverse en una dirección a la vez usando las flechas del teclado. No SHALL poder moverse en dirección opuesta directamente.

#### Scenario: Movimiento hacia arriba
- **WHEN** el jugador presiona la flecha arriba y la dirección actual no es hacia abajo
- **THEN** la serpiente se mueve hacia arriba

#### Scenario: Movimiento hacia abajo
- **WHEN** el jugador presiona la flecha abajo y la dirección actual no es hacia arriba
- **THEN** la serpiente se mueve hacia abajo

#### Scenario: Movimiento hacia la izquierda
- **WHEN** el jugador presiona la flecha izquierda y la dirección actual no es hacia la derecha
- **THEN** la serpiente se mueve hacia la izquierda

#### Scenario: Movimiento hacia la derecha
- **WHEN** el jugador presiona la flecha derecha y la dirección actual no es hacia la izquierda
- **THEN** la serpiente se mueve hacia la derecha

### Requirement: Sistema de puntuación
El juego SHALL otorgar 10 puntos cada vez que la serpiente alcanza una zanahoria.

#### Scenario: Obtener puntuación
- **WHEN** la cabeza de la serpiente coincide con la posición de la zanahoria
- **THEN** el puntaje SHALL aumentar en 10 puntos

### Requirement: Generación de zanahorias
El juego SHALL generar una nueva zanahoria en una posición válida (no sobre la serpiente) cada vez que se consume una.

#### Scenario: Zanahoria en posición válida
- **WHEN** se necesita una nueva posición de zanahoria
- **THEN** el sistema SHALL buscar una posición que no esté ocupada por la serpiente

### Requirement: Colisiones
El juego SHALL terminar cuando la serpiente colisiona con los bordes del canvas o con su propio cuerpo.

#### Scenario: Colisión con borde
- **WHEN** la cabeza de la serpiente supera los límites del canvas
- **THEN** el juego SHALL terminar (Game Over)

#### Scenario: Colisión con cuerpo
- **WHEN** la cabeza de la serpiente coincide con cualquier segmento de su cuerpo
- **THEN** el juego SHALL terminar (Game Over)

### Requirement: Sistema de niveles
El nivel SHALL aumentar cada 100 puntos, incrementando la velocidad del juego.

#### Scenario: Subir de nivel
- **WHEN** el puntaje alcanza un múltiplo de 100
- **THEN** el nivel SHALL aumentar en 1 y la velocidad SHALL incrementarse

### Requirement: Interfaz de usuario
El juego SHALL mostrar puntuación actual, nivel, pantalla de inicio y pantalla de Game Over.

#### Scenario: Mostrar puntuación
- **WHEN** el juego está en curso
- **THEN** la puntuación SHALL ser visible en pantalla

#### Scenario: Pantalla de inicio
- **WHEN** el usuario abre el juego
- **THEN** SHALL mostrar una pantalla de inicio con botón para comenzar

#### Scenario: Pantalla de Game Over
- **WHEN** el juego termina
- **THEN** SHALL mostrar puntuación final y opción para reiniciar