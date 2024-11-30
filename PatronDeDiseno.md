# Patrón de Diseño Strategy.
El patrón Strategy se utiliza para encapsular diferentes comportamientos de membresías (como cálculo de costos o beneficios) en clases separadas, permitiendo que un socio pueda seleccionar dinámicamente la estrategia que corresponda según el tipo de membresía que posea. Esto mejora la flexibilidad y mantenibilidad del sistema de gestión del gimnasio.

# Motivación
El sistema de membresías para los socios del gimnasio puede ser muy diverso. Si las reglas de los diferentes tipos de membresías se colocan en una única clase (como Socio), esto genera un código redundante y difícil de extender. Por ejemplo, al agregar una nueva membresía con reglas diferentes, se tendría que modificar el código existente, lo que puede introducir errores y dificultar el mantenimiento.
El patrón Strategy resuelve este problema al permitir que el comportamiento de cada tipo de membresía (como el cálculo de costos o la activación de beneficios) se gestione de manera independiente en diferentes clases. El socio puede cambiar dinámicamente su estrategia de membresía sin necesidad de modificar otras partes del sistema.

# Estructura de Clases
![image](https://github.com/user-attachments/assets/1586b21d-e5b8-4bbd-a989-9bd9cc3049c8)

# Ejemplo de Código

class MembresiaStrategy:
    method calcularCosto()  
    method otorgarBeneficios()
        

class Membresia inherits MembresiaStrategy:
    method calcularCosto()
        return 100
    method otorgarBeneficios()
        

class MembresiaVIP inherits MembresiaStrategy:
    method calcularCosto()
        return 250
    method otorgarBeneficios()    

class Socio:
    attribute membresía: MembresiaStrategy 
    method asignarMembresia(estrategia: MembresiaStrategy)
        this.membresía = estrategia
    method procesarMembresia()
        costo = membresía.calcularCosto()
        membresía.otorgarBeneficios()
        return costo
