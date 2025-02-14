# Testando convert.com para España

[Tarea en Asana](https://app.asana.com/0/1201820848298280/1208604989923128)

[Páginas web](https://greenpeace.github.io/gpes-test-convert-com/)

## Obervaciones

- Solo el código de seguimiento no pone cookies ⬆︎
- Pone cookies si hay un experimento A/A antes que la persona decida ⬇︎
- El tamaño del script es grande
  - En página en blanco, pero con el tracking de convert.com: 663Kb transferred, 1.3MB resources, 530ms (es bastante) ⬇︎
  - El script que tenemos ahora para AB: 3.4Kb, carga en 110ms ⬆︎
  - Sin tracking convert.com: 1.4MB transferred, 2,7MB resources, 764ms/1.44s
  - Con tracking convert.com: 2.1MB transferred, 4.1MB resources, 930ms/1.85s ⬇︎

Falta conducir más test para ver cuanto afecta al final las páginas de Greenpeace