# What is this?

FlutterMason es un generador de plantillas Flutter que fue desarrollado para mejorar la productividad del desarrollo de aplicaciones Flutter. Este generador de plantillas permite a los desarrolladores crear y consumir plantillas reutilizables, conocidas como "bricks". Un brick puede ser un archivo o una colección de archivos y directorios anidados.

Una vez que las plantillas de brick están definidas, los desarrolladores utilizan la CLI de Mason para crear, administrar y generar nuevos archivos a partir de estos bricks. Mason puede ser muy útil en proyectos más grandes, ya que proporciona una guía definitiva a los desarrolladores y ayuda a mantener la consistencia en el código.

Los bricks utilizan la sintaxis Mustache para agregar variables y condicionales en su archivo. Para definir una variable, puedes usar la notación `{{name}}` en tu código. Luego registra el nombre de la variable en tu archivo `bricks.yaml` para usar esa variable en el momento de la generación de código usando la CLI de Mason.

Además, Mason permite la creación de scripts personalizados de ejecución (Hooks) y la resolución de archivos basada en variables de entrada de ruta utilizando la etiqueta `{{% %}}`.

También es posible tener plantillas anidadas dentro de otras plantillas. Por ejemplo, dada la siguiente estructura:

```
├── HELLO.md
├── {{~ footer.md }}
└── {{~ header.md }}
```

Los `{{~ header.md }}` y `{{~ footer.md }}` son plantillas parciales (plantillas parciales de brick). Las plantillas parciales no se generarán pero pueden incluirse como parte de una plantilla existente.

En resumen, la arquitectura de FlutterMason se basa en la creación y el uso de bricks, que son plantillas reutilizables que pueden ser generadas a partir de archivos y directorios anidados. Estas bricks pueden ser utilizadas para mejorar la eficiencia y la consistencia en el desarrollo de aplicaciones Flutter.
