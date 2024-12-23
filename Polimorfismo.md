## Polimorfismo
Se refiere a la capacidad de los objetos de una misma jerarquía de clases para responder de manera diferente a un mismo mensaje. Esto permite escribir código genérico que puede funcionar con varios tipos de objetos, promoviendo la flexibilidad y la extensibilidad del sistema.

## Ejemplo en el proyecto
![image](https://github.com/user-attachments/assets/e7485880-0b27-4158-8fe0-dc4aa4e6feb4)

Gracias al polimorfismo, el programa puede tratar objetos de Membresía y Membresía VIP de manera uniforme a través de un mismo método. Esto significa que, al invocar este método, un objeto de Membresía VIP puede ejecutar un comportamiento diferente al de un objeto de Membresía, adaptándose a sus características específicas.

## Ejemplo de Código

```java
class Membresia {
    protected String socioId;
    protected LocalDate fechaDeVencimiento;

    public Membresia(String socioId, Date fechaDeVencimiento) {
        this.socioId = socioId;
        this.fechaDeVencimiento = fechaDeVencimiento;
    }

    public boolean comprobarMembresia() {
        return fechaDeVencimiento.after(fecha);
    }
}

class MembresiaVIP extends Membresia {
    private String beneficiosVIP;

    public MembresiaVIP(String socioId, Date fechaDeVencimiento, String beneficiosVIP) {
        super(socioId, fechaDeVencimiento);
        this.beneficiosVIP = beneficiosVIP;
    }
}
```
