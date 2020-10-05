---
description: Configurar tareas periódicas del menú
---

# Tareas periódicas

## Tasks

* Las tareas periódicas a tasks son cosas que ejecutan acciones cada cierto intervalo de tiempo mientras el menú está abierto.
* Cada task está conformada por 3 partes: identificador, intervalo y acciones
* Las tasks del menú se empiezan a ejecutar cuando se abre el menú y dejan de hacerlo cuando se cierra.

**Formas de escribirlo**

* **Normal:** Tasks
* **RegEx:** \(task\|schedule\)\(s\)?

{% tabs %}
{% tab title="EJEMPLO 1" %}
```yaml
Tasks:
  # Identificador del task
  TicTac:
    # Intervalo en ticks
    # 20 ticks = 1 segundo
    period: 20
    # Acciones que se ejcutan
    task:
      - requirement: 'isOperator.'
        actions:
          - 'sound: BLOCK_NOTE_BLOCK_BIT-1-2'
```
{% endtab %}
{% endtabs %}

**Formas de escribir el intervalo**

* **Normal:** period
* **RegEx:** \(period\|time\)\(s\)?

Información adicional:

* Para más información sobre condiciones puedes ir a:

{% page-ref page="../../funciones/condiciones.md" %}

* Para más información sobre acciones puedes ir a:

{% page-ref page="../../acciones/configuracion.md" %}

