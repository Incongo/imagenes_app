📄 Documento: Casos de Uso — Sistema de Gestión de Imágenes
📌 1. Perfiles del sistema
El sistema cuenta con dos tipos de usuarios:

Administrador

Usuario estándar

Cada uno tiene capacidades distintas dentro de la aplicación.

🧑‍💼 2. Casos de uso del Administrador
2.1. Gestión de usuarios
Crear usuarios

Editar usuarios

Eliminar usuarios

Asignar roles (admin / usuario)

Activar o desactivar usuarios

Restablecer contraseñas

2.2. Gestión de roles
Ver roles disponibles

Crear o editar roles (si se habilita)

Asignar permisos globales

(En este proyecto solo existen admin y user, por lo que esta sección es mínima.)

2.3. Gestión de carpetas (estructura jerárquica)
Crear carpetas raíz

Crear subcarpetas

Editar carpetas (nombre, padre)

Mover carpetas dentro de la jerarquía

Eliminar carpetas

Ver toda la estructura completa

Ver estadísticas por carpeta (nº imágenes, tamaño total, etc.)

2.4. Gestión de permisos por carpeta
Asignar permisos a usuarios:

can_view

can_download

can_upload

Revocar permisos

Ver permisos existentes

Copiar permisos entre carpetas

Aplicar permisos a subcarpetas (herencia opcional)

2.5. Gestión de imágenes
Subir imágenes a cualquier carpeta

Subida masiva

Editar metadatos (nombre, etiquetas)

Mover imágenes entre carpetas

Eliminar imágenes

Regenerar thumbnails

Reprocesar EXIF

Ver estadísticas globales (peso total, nº imágenes, etc.)

2.6. Gestión de etiquetas
Crear etiquetas

Editar etiquetas

Eliminar etiquetas

Asignar etiquetas a imágenes

Eliminar etiquetas de imágenes

2.7. Descargas
Descargar imágenes individuales

Descargar imágenes en lote

Generar ZIPs

Ver estado de ZIPs generados

Forzar regeneración de ZIPs

2.8. Sistema de colas (implementación propia)
Ver lista de jobs

Ver estado de jobs

Reintentar jobs fallidos

Cancelar jobs

Lanzar jobs manualmente (regenerar thumbnails, EXIF, etc.)

2.9. Auditoría / Logs
Ver acciones de usuarios

Ver accesos

Ver errores del sistema

Ver estadísticas de uso

👤 3. Casos de uso del Usuario Estándar
3.1. Acceso
Iniciar sesión

Cerrar sesión

Cambiar contraseña

3.2. Navegación por carpetas
Ver solo carpetas con permiso can_view

Ver subcarpetas permitidas

Ver imágenes dentro de carpetas permitidas

3.3. Visualización de imágenes
Ver imagen en tamaño optimizado

Ver imagen original (si tiene permiso can_download)

Ver metadatos EXIF

Ver etiquetas

3.4. Descargas
(Solo si tiene permiso can_download)

Descargar imagen individual

Descargar en tamaño:

original

medium

small

Seleccionar varias imágenes y solicitar ZIP

Ver estado de sus ZIPs

Descargar ZIP cuando esté listo

3.5. Subida de imágenes
(Solo si tiene permiso can_upload)

Subir una imagen

Subir múltiples imágenes

Ver progreso (si se implementa)

Ver errores de subida

3.6. Filtros y búsqueda
Buscar imágenes por nombre

Filtrar por etiquetas

Filtrar por fecha

Filtrar por EXIF:

cámara

fecha de captura

ubicación

ISO

apertura

etc.

3.7. Gestión personal
Ver su perfil

Cambiar contraseña

Ver sus descargas ZIP

Ver sus jobs en cola (solo los suyos)

🎯 Documento guardado
Ya tienes el documento completo con todos los casos de uso.
A partir de aquí podemos:

Derivar requisitos funcionales

Diseñar controladores y acciones

Diseñar servicios

Diseñar middlewares

Diseñar permisos y políticas

Diseñar la base de datos (ya la tenemos)

Diseñar el sistema de colas propio
