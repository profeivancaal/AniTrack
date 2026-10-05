# Changelog

Todos los cambios públicos relevantes de AniTrack Desktop se documentarán en este archivo.

## v1.0.0 — Windows x64

**Estado de publicación:** validación final del hotfix de backup antes de habilitar la descarga pública definitiva.

### Incluido

- Aplicación de escritorio basada en Tauri 2.
- Biblioteca personal con creación, edición y eliminación de registros.
- Seguimiento de episodios y estados personales.
- Favoritos, puntuaciones y notas.
- Búsqueda, filtros y ordenamiento.
- Vista de cuadrícula y lista.
- Estadísticas de la biblioteca.
- Persistencia de biblioteca y preferencias mediante SQLite.
- Portadas almacenadas como archivos locales.
- Exportación e importación de backups JSON compatibles con la biblioteca y portadas.
- Instalador NSIS para Windows x64.
- Accesos de Menú Inicio para AniTrack y su desinstalador.
- Reinstalación y actualización conservando los datos del usuario.
- Funcionamiento offline para el uso normal.

### Hotfix de backup

- Corregida una incompatibilidad entre `mime_type` en Rust y `mimeType` en JavaScript que podía exportar portadas con el tipo MIME vacío.
- La exportación identifica correctamente portadas JPG, JPEG y PNG.
- La importación admite referencias de portada antiguas `cover:` y actuales `file:`.
- Si una portada concreta no puede restaurarse, se conservan los datos del anime y se informa al usuario.
- Las pruebas técnicas de ida y vuelta para JPG y PNG finalizaron correctamente.

### Pendiente antes de publicación definitiva

- Repetir manualmente en la aplicación instalada la prueba completa: **Exportar → vaciar/cambiar biblioteca → Importar → comprobar datos y portada**.

### Notas

- El instalador y el ejecutable todavía no cuentan con firma digital, por lo que Windows puede mostrar el editor como desconocido.
- WebView2 puede requerir descarga durante la instalación si no está presente en Windows.

---

## Próxima etapa

**AniTrack Desktop — Linux Validation**

Objetivos iniciales: Ubuntu, Debian y Zorin OS; evaluación de paquetes `.deb` y AppImage.
