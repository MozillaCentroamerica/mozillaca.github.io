# Plantilla mozilla Centroamerica

Plantilla jekyll realizada con [Creative Theme](http://startbootstrap.com/template-overviews/creative/)

## Si quieres copiar esta plantilla para tu proyecto puedes seguir los siguientes pasos:

- Inicia agregando tu información en el archivo `_config.yml`
- En `_layouts/front.html` ordena las secciones ó eliminalas según tu preferencia.

## Cambios realizados para hacerlo compatible con Jekyll-assets

- Para empezar, los includes por página están dentro de `_includes` y son llamados por las paginas dentro de `_pages`. Seguir el modelo de index.html. No olviden agregar el permalink a cada nueva página, para que `_plugins/page.rb` pueda entender las rutas de cada página y pueda generarse adecuadamente en Github Pages
- Todos los scripts, estilos e imagenes están dentro de `_assets`, el CSS, SCSS y SASS siempre debe estar en la carpeta `_assets/css` como indica jekyll-assets, `main.scss` se mantiene igual, `vendor.sass` toma todos los CSS de terceros (bootstrap, animate etc...). Ambos archivos son compilados y sus versiones CSS llamados dentro de _includes/head.html de esta forma:

```
  {% stylesheet vendor %}
  {% stylesheet main %}
```

- De la misma forma, todo el javascript está integrado en assets/js/all.js y es llamado en front.html, defer:true es solo para que cargue únicamente cuando ha cargado el resto de la página:

```
  {% js all defer:true %}
```

- En `_includes/index/portfolio.html`, puede encontrarse la forma de integrar los archivos dentro de `_assets` al HTML, en este caso imagenes.
- Más información sobre cada cosa y mucho más puede encontrarse en la [documentación](https://github.com/jekyll/jekyll-assets).
