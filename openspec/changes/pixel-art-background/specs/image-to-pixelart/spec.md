## ADDED Requirements

### Requirement: Carga de imagen
El sistema SHALL permitir al usuario cargar una imagen en formato PNG, JPEG o JPG mediante un input file.

#### Scenario: Cargar imagen válida
- **WHEN** el usuario selecciona un archivo PNG, JPEG o JPG
- **THEN** el sistema SHALL procesar la imagen y mostrarla como fondo pixel art

#### Scenario: Formato inválido
- **WHEN** el usuario selecciona un archivo que no es PNG, JPEG o JPG
- **THEN** el sistema SHALL mostrar un mensaje de error

### Requirement: Conversión a pixel art
El sistema SHALL convertir la imagen cargada a pixel art de 30x30 píxeles (tamaño de la cuadrícula del juego).

#### Scenario: Redimensionar imagen
- **WHEN** la imagen es cargada
- **THEN** el sistema SHALL redimensionarla a 30x30 píxeles manteniendo los colores

### Requirement: Fondo del canvas
El sistema SHALL dibujar el pixel art generado como fondo del canvas del juego.

#### Scenario: Mostrar fondo
- **WHEN** el juego se renderiza
- **THEN** el fondo pixel art SHALL ser visible detrás de la serpiente y la comida
