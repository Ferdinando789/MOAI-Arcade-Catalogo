# MOAI Lite Deluxe · Catálogo compartido

Catálogo público de ARCADE. Cualquier usuario puede descargar sin iniciar sesión en GitHub. El proyecto Android se guarda en otro repositorio privado.

## Uso

En MOAI Lite Deluxe v0.1.32 o posterior: ARCADE → Catálogo compartido → elegir juego → Instalar. Motor FBNeo opcional desde ARCADE. Los juegos descargados aparecen en Tus juegos y funcionan sin internet.

## Agregar juegos

Guardar ZIP sin descomprimir en roms/ y añadir la entrada a manifest.json con filename, name, system, description, url, sizeBytes y sha256. Mantener el nombre original de ROM compatible con FBNeo. Publicar únicamente contenido con permiso de distribución.

No guardar aquí claves, contraseñas, tokens ni código privado. Este contenido es público, incluso fuera de la aplicación.

## Juegos agregados

- 1943: The Battle of Midway (Euro): ZIP completo, 38/38 archivos coinciden por tamaño y CRC con FBNeo.
- 1000 Miglia: Great 1000 Miles Rally (94/05/26), gtmrb.zip: set parcial, 5/11 archivos. Requiere el set padre gtmr.zip. Faltan mm-200-402-s0.bin, mm-201-403-s1.bin, mm-202-404-s2.bin, mm-203-405-s3.bin, mm-300-406-a0.bin y mm-100-401-e0.bin. Se conserva el ZIP original sin modificar.

Verificación estática, no ejecución en el Streamer. Fuentes de referencia: https://github.com/finalburnneo/FBNeo/blob/master/src/burn/drv/pre90s/d_1943.cpp y https://github.com/finalburnneo/FBNeo/blob/master/src/burn/drv/pst90s/d_kaneko16.cpp .
