# Testando convert.com para España

[Tarea en Asana](https://app.asana.com/0/1201820848298280/1208604989923128)

[Páginas web](https://greenpeace.github.io/gpes-test-convert-com/)

## Observaciones de pruebas realizadas

### Cookies

- Para no poner cookies hay que primero añadir el en global javascript:

```javascript
_conv_q.push(["consentRequired"]);
```

Y después gestionar los permisos de cookies con la interfaz de tracking y el GUI.


### Tamaño del script

- El tamaño del script es grande
  - En página en blanco, pero con el tracking de convert.com: 663Kb transferred, 1.3MB resources⬇︎
  - Como referencia de comparación el script de ahora para AB: 3.4Kb ⬆︎
- Comparación de la home aislada:
  - Sin tracking convert.com: 1.4MB transferred, 2,7MB resources (referencia)
  - Misma página con tracking convert.com: 2.1MB transferred, 4.1MB resources ⬇︎

## Por hacer

### Cookies

- Integrar la autorización de cookies con el GUI y sistema de gestión de cookies de Greenpeace.


### Velocidad

- Falta conducir más test para ver cuanto afecta al final las páginas de Greenpeace. Con conexiones rápidas y ordenador potente el efecto no es demasiado grave (aunque afecta a todas las páginas sin experimento)
- Puede afectar mucho al SEO, sobretodo si pasa las paginas a rojo.
- Falta simular el uso de la pagina con conexiones menos buenas.


