# Actualizaciones de MOAI Lite Deluxe

Este directorio distribuye únicamente APKs firmadas y sus metadatos públicos. El código completo y la clave de firma se conservan en el repositorio privado de la aplicación.

MOAI v0.1.38 o posterior consulta latest.json al abrirse, como máximo cada 6 horas, y descarga las versiones nuevas en segundo plano. Configuración → Actualizaciones de MOAI permite buscar manualmente, desactivar la descarga automática o abrir el instalador. Android solicita confirmar la instalación y, cuando corresponde, autorizar esta fuente.

Para publicar otra versión: compilar con la misma firma e incrementar versionCode; verificar sus pruebas y firma; subir MOAI-Lite-Deluxe-vX.Y.Z.apk aquí; verificar la descarga pública; actualizar latest.json con schemaVersion=1, applicationId, versionCode, versionName, minSdk, url, sizeBytes y sha256 exactos. Publicar los metadatos al final, una vez disponible la APK. No reutilizar URLs de versiones anteriores.

No subir proyectos, contraseñas, tokens ni archivos de firma a este repositorio.
