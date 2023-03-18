---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
title: Inicio
---

<script>
    // This variable will save the event for later use.
let deferredPrompt;
window.addEventListener('beforeinstallprompt', (e) => {
  // Prevents the default mini-infobar or install dialog from appearing on mobile
  e.preventDefault();
  // Save the event because you'll need to trigger it later.
  deferredPrompt = e;
  // Show your customized install prompt for your PWA
  // Your own UI doesn't have to be a single element, you
  // can have buttons in different locations, or wait to prompt
  // as part of a critical journey.
  showInAppInstallPromotion();
});
    function install(){
        deferredPrompt.prompt()
    }
</script>

Hola.

Am... bien, supongo que te estarás preguntando _"¿Qué es esto?"_. Es normal, página rara, poca información...

Esto es un **Baul**, es donde guardo las cosas que escribo: historias, textos de práctica o ideas. Muchas de ellas no están revisadas, o acabadas si quiera, y tendrán faltas de ortografía o directamente fallos en la historia.
Pero són lo que són, práctica y pruebas.

Si eso no te echa para atrás y te puede la curiosidad, hecha un vistazo al apartado de [post](/post) y divierteté.

Además, puedes guardar esta página como una "aplicación" tocando [instalar](#install).

<button id="install" class="cool-btn" onclick="install()">Instalar</button>

Gracias.
