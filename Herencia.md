## Herencia

## Ejemplo en el proyecto
![image](https://github.com/user-attachments/assets/56abbe4f-217d-47a3-99a7-a7cc59ad0920)

## Ejemplo de Código

```java
public class Usuario {
    private String nombre;

    public Usuario(String nombre) {
        this.nombre = nombre;
    }

    public String getNombre() {
        return nombre;
    }
}

public class Socio extends Usuario {
    public Socio(String nombre) {
        super(nombre);
    }
}

public class Entrenador extends Usuario {
    public Entrenador(String nombre) {
        super(nombre);
    }
}
```
