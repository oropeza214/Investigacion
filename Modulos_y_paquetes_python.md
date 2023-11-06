# Módulos y Paquetes en Python

## ¿Qué son los Módulos y Paquetes?

En Python, tanto los módulos como los paquetes se utilizan para organizar el espacio de nombres del código y promover su reutilización.

### Módulos

Un **módulo** es un archivo de Python que contiene definiciones y declaraciones de variables, funciones, clases o cualquier otro objeto de Python. El nombre del archivo se convierte en el nombre del módulo.

#### Ejemplo de un Módulo:

```python
# archivo: mi_modulo.py

def saluda(nombre):
    print("Hola", nombre)
```

## Paquetes

Un paquete es una forma de coleccionar varios módulos en una sola jerarquía de directorios. Un paquete tiene una estructura de directorio particular y contiene un archivo especial llamado __init__.py.

```lua
mi_paquete/
|-- __init__.py
|-- modulo1.py
|-- modulo2.py
```

Los archivos modulo1.py y modulo2.py son módulos que forman parte del paquete mi_paquete.

Para utilizar un módulo dentro de este paquete, lo importarías de la siguiente manera:

```python
# otro_archivo.py

from mi_paquete import modulo1

modulo1.funcion_del_modulo()
```

### ¿Por qué se llaman distintos?

Módulo: Es la unidad más pequeña de código reutilizable, simplemente un archivo.
Paquete: Es una colección de módulos que permite una gestión y organización más compleja del código.

### Diferencias entre Módulos y Paquetes

La principal diferencia es la estructura. Mientras que un módulo es un solo archivo, un paquete es un directorio que puede contener múltiples módulos y subpaquetes.

### Uso Práctico

El uso de módulos y paquetes ayuda a mantener el código organizado, reusable y legible. Los paquetes pueden agrupar módulos relacionados bajo un mismo contexto y resolver posibles conflictos de nombres en espacios de nombres grandes.

Por ejemplo, el paquete requests contiene varios módulos que manejan diferentes aspectos de las solicitudes HTTP. Al instalar el paquete con pip install requests, puedes usar todas las funciones relacionadas con HTTP que están bien organizadas en módulos dentro del paquete.

```python
import requests

response = requests.get('https://api.github.com')
```

## Conclusión

Los módulos y paquetes son fundamentales para una buena arquitectura de software en Python. Facilitan el mantenimiento y la colaboración en proyectos de software grandes y complejos.

