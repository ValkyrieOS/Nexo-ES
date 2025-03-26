# Nexo ES - Servidor Alpha

Este es el sitio web oficial del servidor Nexo ES, actualmente en fase Alpha.

## Estructura del Proyecto

- `index.html`: Página principal del sitio web
- `changelog.html`: Página que muestra todas las actualizaciones del servidor
- `changelogs/`: Directorio que contiene los archivos HTML individuales para cada actualización
- `img/`: Directorio que contiene las imágenes del sitio
- `generate_changelog.py`: Script de Python para generar nuevas entradas de changelog

## Cómo Usar el Generador de Changelogs

Para añadir una nueva entrada al changelog, ejecuta el script `generate_changelog.py` y sigue las instrucciones:

```
python generate_changelog.py
```

El script te pedirá:
1. Título del changelog
2. Fecha (en formato DD/MM/YYYY)
3. Descripción general de la actualización
4. Lista de cambios específicos

Una vez completado, el script:
1. Creará un nuevo archivo HTML en el directorio `changelogs/`
2. Actualizará `changelog.html` con un enlace a la nueva entrada
3. Actualizará `index.html` para mostrar las 3 actualizaciones más recientes

## Ejemplo de Uso desde Otro Script

```python
from generate_changelog import create_changelog_entry

create_changelog_entry(
    "Actualización Alpha 0.1", 
    "01/01/2023", 
    "Primera actualización del servidor con nuevas características.", 
    [
        "Añadido sistema de rangos", 
        "Mejorado el rendimiento del servidor", 
        "Corregidos errores menores"
    ]
)
```

## Tecnologías Utilizadas

- HTML5
- Tailwind CSS (vía CDN)
- Python (para la generación de changelogs estáticos)