## Herencia

## Ejemplo en el proyecto
![image](https://github.com/user-attachments/assets/56abbe4f-217d-47a3-99a7-a7cc59ad0920)

## Ejemplo de Código

```java
public class Usuario {
    protected String userId;
    protected String contraseña;
    protected Date fechaRegistro;

    public Usuario(String userId, String contraseña, Date fechaRegistro) {
        this.userId = userId;
        this.contraseña = contraseña;
        this.fechaRegistro = fechaRegistro;
    }

    public boolean confirmarInicioDeSesion(String inputPassword) {
        return this.contraseña.equals(inputPassword);
    }
}

public class Socio extends Usuario {
    private String membresia;

    public Socio(String userId, String contraseña, Date fechaRegistro, String membresia) {
        super(userId, contraseña, fechaRegistro);
        this.membresia = membresia;
    }


public class Entrenador extends Usuario {
    private boolean disponibilidad;

    public Entrenador(String userId, String contraseña, Date fechaRegistro, boolean disponibilidad) {
        super(userId, contraseña, fechaRegistro);
        this.disponibilidad = disponibilidad;
    }
}
```
