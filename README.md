<!-- Correcciones gemini 11-17-2026 -->
# mi-portafolio
### Aprendizajes en HTML Semántico

* **Atributos `id` consistentes:**
  * **Mi error:** Mezclar mayúsculas y minúsculas (`id="Habilidades"` vs. `id="metas"`) y dejar la primera `<section>` sin `id`.
  * **Regla aplicada:** Escribir todos los `id` en minúsculas, sin tildes ni espacios (`kebab-case`, ej. `id="sobre-mi"`), e identificar cada sección para evitar fallos en CSS y JS.
* **Ortografía en etiquetas (`<footer>`):**
  * **Mi error:** Escribir `<foorter>` con una letra `r` de más en la apertura y el cierre.
  * **Regla aplicada:** Verificar el nombre exacto de las etiquetas semánticas (`<footer>`), ya que un error tipográfico hace que el navegador la trate como un elemento desconocido y afecta la accesibilidad.

<!-- Correcciones gemini 11-18-2026 -->
## Correcciones y mejoras de HTML Semántico y Jerarquía

### 1. `<main>` anidado dentro de `<header>` (en las páginas de proyectos y contacto)
* **Qué mejorar:** En las páginas de proyectos y contacto, la etiqueta `<main>` está colocada dentro de `<header>`, y `</header>` cierra hasta después de `</main>`. `<header>` debe contener solo la cabecera/navegación y cerrarse antes de abrir `<main>`[cite: 21, 22].
* **Por qué:** `<header>` representa la introducción o navegación de la página/sección, mientras que `<main>` representa el contenido principal único del documento[cite: 21]. Mezclar `<main>` dentro de `<header>` rompe la estructura semántica y confunde a los lectores de pantalla y a los buscadores[cite: 21].
* **Corrección:** Cierra `</header>` justo después de `</nav>` y abre `<main>` como un elemento hermano de `<header>` y `<footer>`[cite: 21, 22].

### 2. Atributos duplicados/mal formados en `<img>` (página principal)
* **Qué mejorar:** En la etiqueta `<img>` de tu foto aparecen repetidos `width="200" height="200"` y luego `width"300" height"300"` (sin el signo `=` en el segundo par).
* **Por qué:** Los atributos duplicados o sin `=` son HTML inválido que el validador del W3C marcará como error, además de generar ambigüedad en las dimensiones reales de la imagen[cite: 23, 26].
* **Corrección:** Deja un solo par de atributos bien escritos, por ejemplo `width="200" height="200"`[cite: 23].

### 3. Falta de encabezados `<h2>` en secciones (página principal y contacto)
* **Qué mejorar:** En la página de contacto usas `<p>Mis datos Personales</p>` para titular la sección en lugar de un encabezado (`<h2>`), y en la página principal conviene revisar que cada `<section>` tenga su título jerárquico claro.
* **Por qué:** Las etiquetas `<section>` normalmente van acompañadas de un encabezado para definir su tema y construir un esquema claro de la página[cite: 21, 22]. Usar solo `<p>` no le da jerarquía estructural al bloque.
* **Corrección:** Cambia `<p>Mis datos Personales</p>` por `<h2>Mis datos personales</h2>`[cite: 22].

### 4. Uso de `<nav>` secundario para enlaces de correo y teléfono (página de contacto)
* **Qué mejorar:** En la sección de contacto envuelves los enlaces de `mailto:` y `tel:` dentro de una segunda etiqueta `<nav>`.
* **Por qué:** `<nav>` está pensado para bloques principales de navegación del sitio (menús de páginas o secciones clave), no para cualquier grupo de enlaces puntuales de contacto[cite: 21].
* **Corrección:** Deja la lista `<ol>` directamente dentro de `<section>` (o dentro de un `<address>` si corresponde a datos de contacto), reservando `<nav>` para el menú de navegación principal[cite: 21].

### 5. Títulos `<title>` genéricos y ortografía/tildes en textos visibles
* **Qué mejorar:** En las páginas secundarias aparece `<title>Document</title>`, y en los textos visibles hay detalles como `"Souy"`, `"Castellon"` sin tilde, `"Escribime"` / `"Llamame"` sin tilde, `"vídeo_reflexion.mp4"` con tilde en la ruta del archivo y mayúsculas/minúsculas inconsistentes (`"metas"`, `"habilidades"`, `"proyecto"`).
* **Por qué:** Cada página necesita un `<title>` único y descriptivo para SEO y usabilidad, y evitar tildes o caracteres especiales en nombres de archivos/carpetas previene rutas rotas en servidores o sistemas sensibles a mayúsculas/minúsculas[cite: 24]. Además, `<html lang="es">` indica que el contenido está en español correcto[cite: 19].
* **Corrección:** Asigna un `<title>` propio a cada página (ej. `Proyectos | Samuel Castellón` y `Contacto | Samuel Castellón`), corrige la ortografía visible y renombra el archivo de video sin tilde (ej. `media/video-reflexion.mp4`) actualizando el `href`.

### 6. Bloques duplicados al pegar el código
* **Qué mejorar:** Al pegar los tres archivos HTML juntos, el bloque de la página de contacto aparece repetido varias veces.
* **Por qué:** Tener código duplicado en un mismo archivo o repositorio genera confusión al revisar o validar cada página por separado.
* **Corrección:** Asegúrate de mantener cada página (`index.html`, `proyectos.html` y `contacto.html`) en su propio archivo independiente y limpio[cite: 17, 24].