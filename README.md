# Testando convert.com para España

[Tarea en Asana](https://app.asana.com/0/1201820848298280/1208604989923128)

[Páginas web](https://osvik.github.io/test-convert-temp/)


- [Testando convert.com para España](#testando-convertcom-para-españa)
  - [Observaciones de pruebas realizadas](#observaciones-de-pruebas-realizadas)
    - [Cookies](#cookies)
    - [Tamaño del script](#tamaño-del-script)
    - [Velocidad](#velocidad)


## Observaciones de pruebas realizadas

### Cookies

Para no poner cookies hay que primero añadir el en global javascript:

```javascript
_conv_q.push(["consentRequired"]);
```

Y después se gestionan los permisos de cookies con la interfaz de tracking y el GUI.

La implementación tiene algún tipo de bug porque el código arriba no aparece de inmediato. Se desconoce aún si la solución es borrar todos los experimentos o si con el pasar del tiempo de actualiza.


### Tamaño del script

- El tamaño del script es grande
  - En página en blanco, pero con el tracking de convert.com: 663Kb transferred, 1.3MB resources⬇︎
  - Como referencia de comparación el script de ahora para AB: 3.4Kb ⬆︎
- Comparación de la home aislada:
  - Sin tracking convert.com: 1.4MB transferred, 2,7MB resources (referencia)
  - Misma página con tracking convert.com: 2.1MB transferred, 4.1MB resources ⬇︎

### Velocidad

Comparando la página con script versus sin script convert:

- [Sin script](https://greenpeace.github.io/gpes-test-convert-com/off.html)
- [Con script y un experimento muy simple](https://greenpeace.github.io/gpes-test-convert-com/convert-2.html)

Pagespeed:

- [Pagespped sin convet](https://pagespeed.web.dev/analysis/https-greenpeace-github-io-gpes-test-convert-com-off-html/nbspszzj83?form_factor=mobile)
- [Pagespeed con convert](https://pagespeed.web.dev/analysis/https-greenpeace-github-io-gpes-test-convert-com-convert-2-html/blhiugl2n6?form_factor=mobile)

WebPageTest:

- [WebPageTest sin convert](https://www.webpagetest.org/result/250219_BiDc20_6XA/)
- [WebPageTest con convert](https://www.webpagetest.org/result/250219_AiDcRJ_6VB/)

- [Tiempos sin convert](tests/webpagetest-sin-convert.png)
- [Tiempos con convert](tests/webpagetest-con-convert.png)


