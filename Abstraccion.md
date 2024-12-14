## Abstracción
Consiste en simplificar la complejidad del mundo real modelando solo los aspectos esenciales relevantes para el sistema. Los objetos abstractos representan entidades del dominio de aplicación y sus interacciones, lo que facilita la comprensión y el diseño del software.

## Ejemplo en el proyecto
![image](https://github.com/user-attachments/assets/8cc8ecfb-7dd3-46d3-838c-86a484485ca8)

## Ejemplo de Código

Gracias a la abstracción, la clase Equipo encapsula información esencial sobre los equipos del gimnasio. Si requiere mantenimiento, le deja los detalles específicos del mantenimiento a la clase Mantenimiento. Esto permite modelar los aspectos relevantes del equipo y su mantenimiento sin complicar el diseño, facilitando la extensión o modificación del sistema en el futuro.

```java
public class Equipo {
    private String tipoDeEquipo;
    private String estadoDelEquipo;
    private boolean mantenimientoRequerido;

    public boolean solicitarMantenimiento() {
        if (estadoDelEquipo.equals("defectuoso")) {
            mantenimientoRequerido = true;
            return true;
        }
        return false;
    }
}
```
