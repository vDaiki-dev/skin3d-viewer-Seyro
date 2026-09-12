# Skin3D Viewer Seyro

Visor interactivo de skins de Minecraft en 3D, creado para cargar, visualizar y explorar skins desde el navegador con una interfaz retro inspirada en los menús pixel-art.

El proyecto está pensado para funcionar como una página estática en **GitHub Pages**, sin servidor propio ni proceso de compilación. La versión actual utiliza `index.html` y un archivo de audio local opcional.

## Demo

La página puede publicarse directamente con GitHub Pages desde la rama `main` del repositorio.

## Características

| Función | Descripción |
|---|---|
| Visor 3D | Modelo de jugador de Minecraft renderizado en el navegador. |
| Carga por usuario | Permite buscar skins mediante un nombre de usuario de Minecraft. |
| Carga local | Permite seleccionar o arrastrar un archivo `.png` de skin. |
| Detección de modelo | Detecta automáticamente el modelo clásico o slim cuando la opción de forzado está desactivada. |
| Capas 3D | Incluye una vista experimental de las capas externas y un control de separación. |
| Animaciones | Incluye idle, walk, run, wave, fly y stop. |
| Cámara | Permite rotar y hacer zoom con el mouse o la pantalla táctil. |
| Iluminación | Incluye intensidad global y varios colores de luz. |
| Capas y elytra | Permite mostrar u ocultar la capa cargada. |
| Audio | Incluye reproducción manual y control de volumen para `musica.mp3`. |
| Exportación | Permite guardar una captura PNG del visor. |
| Diseño responsive | Se adapta a pantallas pequeñas y dispositivos móviles. |

## Archivos del proyecto

```text
index.html   # Aplicación completa: estructura, estilos y JavaScript
musica.mp3   # Música opcional, no incluida en este repositorio por motivos de distribución
```

El archivo `fondo.mp4` no forma parte de la versión actual porque su tamaño era demasiado grande para utilizarlo cómodamente en GitHub Pages.

## Uso local

Descarga o clona el repositorio y abre `index.html` en un navegador moderno. Para probar la música, coloca un archivo llamado `musica.mp3` junto al HTML y pulsa el botón **MUSIC: OFF**.

Algunos navegadores pueden limitar ciertas solicitudes cuando un archivo HTML se abre directamente mediante `file://`. Si la carga por nombre de usuario no funciona localmente, puedes iniciar un servidor estático sencillo desde la carpeta del proyecto:

```bash
python3 -m http.server 8000
```

Después visita [http://localhost:8000](http://localhost:8000).

## Publicación con GitHub Pages

1. Sube `index.html` al directorio principal del repositorio.
2. Sube `musica.mp3` únicamente si tienes derecho a redistribuirlo.
3. En GitHub, abre **Settings → Pages**.
4. Selecciona la rama `main` y la carpeta raíz `/ (root)`.
5. Guarda la configuración y espera a que GitHub Pages genere el sitio.

GitHub Pages puede tardar unos minutos en mostrar los cambios. Si el navegador conserva una versión anterior, utiliza una recarga forzada con `Ctrl + F5`.

## Tecnologías utilizadas

- HTML5, CSS3 y JavaScript sin framework.
- [skinview3d](https://github.com/bs-community/skinview3d) para el visor de skins y el renderizado 3D.
- [Three.js](https://threejs.org/) mediante la dependencia utilizada por `skinview3d`.
- [Google Fonts](https://fonts.google.com/) para las tipografías `Press Start 2P` y `VT323`.
- [MC-Heads](https://mc-heads.net/) como fuente de skins para la búsqueda por nombre de usuario.

## Créditos y atribuciones

Este proyecto combina trabajo propio, asistencia de herramientas de inteligencia artificial e ideas y referencias de proyectos relacionados con la visualización de modelos de Minecraft. La distribución aproximada de participación indicada por el autor es la siguiente:

| Participación aproximada | Autor o fuente | Aporte |
|---:|---|---|
| 40% | **Seyro / vDaiki-dev** | Diseño del proyecto, dirección visual, integración, decisiones de funcionalidad, pruebas y publicación. |
| 50% | **cosmic-fi — skin3d** | Referencia e inspiración para la idea del visor, sus funciones y el enfoque general de visualización 3D. Repositorio: [cosmic-fi/skin3d][1]. |
| 10% | **Claude** | Apoyo para estructurar, revisar y depurar partes del HTML, CSS y JavaScript. |

### Nota sobre `skin3d` y `skinview3d`

El repositorio de referencia `cosmic-fi/skin3d` es una fuente de inspiración y consulta para este proyecto. La implementación actual del archivo `index.html` utiliza la librería [`skinview3d`][2] desde un CDN, por lo que no debe afirmarse que este repositorio contiene una copia directa de `cosmic-fi/skin3d`.

La atribución anterior describe la influencia y las referencias utilizadas durante el desarrollo, no una afirmación de autoría sobre el código de terceros.

## Crédito de la música

La música utilizada durante el desarrollo y prevista para el archivo local `musica.mp3` es **“Blue Boi” de Lakey Inspired**.

Fuente compartida por el autor:

[Blue Boi — Lakey Inspired, versión compartida en YouTube][3]

Antes de redistribuir `musica.mp3` dentro de un repositorio público, comprueba que la licencia o los permisos del archivo permiten su publicación y reproducción en una página web. Este README acredita la fuente, pero no sustituye la autorización del titular de los derechos.

## Licencia

El código original de este proyecto no incluye todavía una licencia propia. Si quieres permitir que otras personas lo reutilicen legalmente, añade un archivo `LICENSE` con una licencia elegida por ti, por ejemplo MIT.

Las librerías, fuentes, servicios, imágenes, skins y música de terceros mantienen sus propias licencias y condiciones de uso. Consulta sus fuentes originales antes de redistribuirlos.

## Estado del proyecto

El proyecto se encuentra en desarrollo personal. Algunas funciones, como la separación experimental de capas 3D y la detección de ciertas estructuras internas del modelo, pueden depender de la versión de la librería utilizada en el CDN.

## Referencias

[1]: https://github.com/cosmic-fi/skin3d "cosmic-fi/skin3d — biblioteca y referencia de visualización de modelos de Minecraft"
[2]: https://github.com/bs-community/skinview3d "skinview3d — biblioteca JavaScript para visualizar skins de Minecraft"
[3]: https://youtu.be/KVOIXy40KJ0?si=twjsEN3E_7GxQn1t "Blue Boi — Lakey Inspired, enlace compartido por el autor"
[4]: https://pages.github.com/ "GitHub Pages — documentación oficial"
[5]: https://threejs.org/ "Three.js — biblioteca JavaScript 3D"
[6]: https://mc-heads.net/ "MC-Heads — servicio de skins de Minecraft"

---

Creado por **Seyro / vDaiki-dev**.

Si reutilizas partes de este proyecto, conserva los créditos de las librerías, servicios y recursos de terceros.
