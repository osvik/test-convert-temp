# Testando convert.com para España

[Tarea en Asana](https://app.asana.com/0/1201820848298280/1208604989923128)

[Páginas web](https://greenpeace.github.io/gpes-test-convert-com/)

## Observaciones de pruebas realizadas

### Cookies

- Solo con el código de seguimiento y sin experimento pone cookies ⬇︎
- Pone cookies si hay un experimento A/A antes que la persona decida ⬇︎

### Tamaño del script

- El tamaño del script es grande
  - En página en blanco, pero con el tracking de convert.com: 663Kb transferred, 1.3MB resources⬇︎
  - Como referencia de comparación el script de ahora para AB: 3.4Kb ⬆︎
- Comparación de la home aislada:
  - Sin tracking convert.com: 1.4MB transferred, 2,7MB resources (referencia)
  - Misma página con tracking convert.com: 2.1MB transferred, 4.1MB resources ⬇︎

## Por hacer

### Cookies

- Falta ver si se puede controlar el uso de cookies, para que se pongan solo después de la aceptación.

### Velocidad

- Falta conducir más test para ver cuanto afecta al final las páginas de Greenpeace. Con conexiones rápidas y ordenador potente el efecto no es demasiado grave (aunque afecta a todas las páginas sin experimento)

