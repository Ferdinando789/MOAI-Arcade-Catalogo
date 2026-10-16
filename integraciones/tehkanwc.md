# Tehkan World Cup (1985) — integración MOAI Arcade

Estado: **perfil de controles preparado; no publicado en catálogo instalable**. No hay ROM verificada ni autorización de distribución. No anunciarlo como funcional hasta probarlo en Google TV Streamer.

## Referencia del motor
- FBNeo: https://github.com/finalburnneo/FBNeo/blob/master/src/burn/drv/pre90s/d_tehkanwc.cpp
- Nombre del set: `tehkanwc.zip`.
- El archivo C++ es el driver del emulador, **no** contiene los datos de la ROM.
- El driver declara `p1 coin`, `p1 start`, `p1 fire 1`, ejes X/Y relativos y `p1 right/left/down/up` (igualmente para P2).
- **Importante**: FBNeo implementa `BurnTrackballUDLR` para convertir los botones digitales en desplazamientos del trackball; no hace falta modificar el driver para usar cruceta.

## Perfil de controles esperado (Android/Google TV)
| Acción | Gamepad | Remoto TV |
| --- | --- | --- |
| Mover P1 | Cruceta o stick izquierdo → `p1 up/down/left/right` | Flechas → mismas entradas |
| Patear | A → `p1 fire 1` | OK → `p1 fire 1` durante partida |
| Ficha | Select / View → `p1 coin` | Menú en pantalla «Insertar ficha» |
| Iniciar | Start / Menu → `p1 start` | Menú en pantalla «Iniciar» |
| Volver | Back / B → salir al menú MOAI (sin inyectarlo al juego) | Atrás → salir / volver |
| Segundo jugador | Segundo gamepad con entradas P2 | No requerido |

Evitar que OK active Start y Patear simultáneamente. En remoto, ofrecer acciones de ficha e inicio en un menú superpuesto, ya que muchos mandos no tienen botones Select ni Start. Conservar movimiento y un botón de acción durante el partido.

## Criterios de validación antes de publicar
1. Tener un set ROM obtenido y compartido legítimamente y verificar nombres internos, CRC/tamaño según driver FBNeo, SHA-256 del ZIP y arranque real.
2. Confirmar que el adaptador Android del motor pasa entradas digitales a `p1 up/down/left/right` (no ejes analógicos absolutos); probar diagonales, giro y velocidad.
3. Probar ficha, inicio, disparo/pase, retorno al menú y segundo gamepad.
4. Probar en Google TV Streamer 4K, incluyendo control remoto.
5. Solo entonces colocar el ZIP autorizado en `roms/tehkanwc.zip` y añadir `manifest.json` con `filename`, `name`, `system`, `description`, `url`, `sizeBytes` y `sha256`.

Este documento es un plan técnico de integración, no una implementación ni una prueba de funcionamiento.
