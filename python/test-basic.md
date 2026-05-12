
# Python test

## Indice

- [Python test](#python-test)
  - [Indice](#indice)
  - [Sobre los test](#sobre-los-test)
    - [Que son los test](#que-son-los-test)
    - [Ventajas](#ventajas)
    - [Desventajas](#desventajas)
    - [Tipos de pruebas](#tipos-de-pruebas)
    - [Como funcionan las pruebas](#como-funcionan-las-pruebas)
    - [Como se estructuran](#como-se-estructuran)
  - [Test](#test)
    - [Unittest](#unittest)
    - [Pytest](#pytest)
    - [Bruno](#bruno)

---

## Sobre los test

### Que son los test

Son un conjunto de técnicas y herramientas que permiten verificar el correcto funcionamiento de un programa o módulo de código. Consisten en escribir código adicional que ejecuta y valida el comportamiento esperado de la aplicación.

### Ventajas

- **Eficiencia**: Permiten detectar errores temprano, reduciendo el tiempo y costo de corrección.

- **Repetibilidad**: Las pruebas se pueden ejecutar múltiples veces de manera automática, garantizando consistencia.

- **Integración CI/CD**: Facilitan la integración continua y el despliegue continuo, automatizando el proceso de verificación.

- **Documentación viva**: Las pruebas sirven como documentación del comportamiento esperado del código.

- **Refactorización segura**: Permiten modificar el código con confianza, sabiendo que las pruebas detectarán cualquier ruptura.

- reportabilidad:

- Mayor cobertura:

### Desventajas

- **Tiempo inicial**: Requiere tiempo adicional para escribir y mantener las pruebas.

- **Complejidad**: Para sistemas complejos, diseñar pruebas exhaustivas puede ser desafiante.

- **Falsos positivos/negativos**: Pruebas mal diseñadas pueden dar resultados incorrectos.

- **Mantenimiento**: Las pruebas deben actualizarse cuando cambia el código.

### Tipos de pruebas

- **Regresión**: Verifican que cambios recientes no hayan roto funcionalidades existentes.

- **Unitarias**: Prueban componentes individuales del código (funciones, clases) de forma aislada.

- **Integración**: Verifican la interacción entre diferentes componentes o módulos.

- **Funcionales**: Evalúan el comportamiento completo del sistema desde la perspectiva del usuario.

- **Rendimiento**: Miden el tiempo de ejecución y el uso de recursos.

- **Aceptación**: Validan que el software cumple con los requisitos del cliente.

### Como funcionan las pruebas

Las pruebas funcionan mediante la ejecución de código de prueba que invoca el código bajo prueba con datos de entrada específicos y compara los resultados obtenidos con los resultados esperados. Si coinciden, la prueba pasa; si no, falla. Se utilizan frameworks como unittest o pytest para estructurar y ejecutar estas pruebas de manera organizada.

### Como se estructuran

Las pruebas se estructuran típicamente en archivos separados (generalmente en una carpeta `tests/`), con nombres que reflejan el módulo que prueban (ej. `test_mymodule.py`). Cada archivo contiene clases de prueba que heredan de una clase base del framework, y métodos que representan pruebas individuales. Se siguen convenciones como el patrón AAA (Arrange, Act, Assert) para organizar cada prueba.

## Test

### Unittest

### Pytest



### Bruno