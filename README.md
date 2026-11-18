# mi-portafolio
### Aprendizajes en HTML Semántico

* **Atributos `id` consistentes:**
  * **Mi error:** Mezclar mayúsculas y minúsculas (`id="Habilidades"` vs. `id="metas"`) y dejar la primera `<section>` sin `id`.
  * **Regla aplicada:** Escribir todos los `id` en minúsculas, sin tildes ni espacios (`kebab-case`, ej. `id="sobre-mi"`), e identificar cada sección para evitar fallos en CSS y JS.
* **Ortografía en etiquetas (`<footer>`):**
  * **Mi error:** Escribir `<foorter>` con una letra `r` de más en la apertura y el cierre.
  * **Regla aplicada:** Verificar el nombre exacto de las etiquetas semánticas (`<footer>`), ya que un error tipográfico hace que el navegador la trate como un elemento desconocido y afecta la accesibilidad.
