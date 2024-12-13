## Encapsulamiento

## Ejemplo en el proyecto
![image](https://github.com/user-attachments/assets/a1afa160-828d-49f2-98b2-d8b0c4dba7a2)

## Ejemplo de Código

```java
public class Socio {
    private String direccion;
    private String telefono;

    public Socio(String direccion, String telefono) {
        this.direccion = direccion;
        this.telefono = telefono;
    }

    public void actualizarDatos(String nuevaDireccion) {
        if (validarDireccion(nuevaDireccion)) {
            this.direccion = nuevaDireccion;
        } else {
            throw new IllegalArgumentException("Dirección inválida");
        }
    }

    public void actualizarTelefono(String nuevoTelefono) {
        if (validarNumero(nuevoTelefono)) {
            this.telefono = nuevoTelefono;
        } else {
            throw new IllegalArgumentException("Número inválido");
        }
    }

    private boolean validarDireccion(String direccion) {
        return direccion != null;
    }

    private boolean validarNumero(String numero) {
        return numero != null;
    }

    public String getDireccion() {
        return direccion;
    }

    public String getTelefono() {
        return telefono;
    }
  }
```
