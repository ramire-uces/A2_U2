## Encapsulación
Es el proceso de ocultar la implementación interna de un objeto y exponer sólo las interfaces públicas. Esto permite que los objetos mantengan su estado interno protegido de accesos no autorizados, promoviendo así la modularidad y la seguridad del sistema.

## Ejemplo en el proyecto
![image](https://github.com/user-attachments/assets/a1afa160-828d-49f2-98b2-d8b0c4dba7a2)

En la clase Socio, atributos como nombre o membresía están restringidos y se gestionan mediante métodos como registrar() o actualizarDatos(). Lo mismo ocurre con las clases Dirección y Teléfono, que validan sus datos con métodos como validarDirección() y validarNúmero().

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
