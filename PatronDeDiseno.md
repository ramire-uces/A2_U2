# Patrón de Diseño seleccionado: Strategy.
El patrón Strategy se utiliza para encapsular diferentes comportamientos de membresías (como cálculo de costos o beneficios) en clases separadas, permitiendo que un socio pueda seleccionar dinámicamente la estrategia que corresponda según el tipo de membresía que posea. Esto mejora la flexibilidad y mantenibilidad del sistema de gestión del gimnasio.

# Motivación
El sistema de membresías para los socios del gimnasio puede ser muy diverso. Si las reglas de los diferentes tipos de membresías se colocan en una única clase (como Socio), esto genera un código redundante y difícil de extender. Por ejemplo, al agregar una nueva membresía con reglas diferentes, se tendría que modificar el código existente, lo que puede introducir errores y dificultar el mantenimiento.
