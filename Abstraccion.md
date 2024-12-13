## Abstracción

## Ejemplo en el proyecto
![image](https://github.com/user-attachments/assets/8cc8ecfb-7dd3-46d3-838c-86a484485ca8)

## Ejemplo de Código

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
