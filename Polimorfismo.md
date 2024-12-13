## Polimorfismo

## Ejemplo en el proyecto
![image](https://github.com/user-attachments/assets/e7485880-0b27-4158-8fe0-dc4aa4e6feb4)

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
