# 🚀 Framework de Automatización Web

Framework de automatización web diseñado para ejecutar pruebas de regresión de forma eficiente, manteniendo código limpio, escalable y con reportes detallados.

---

## 🧰 Tecnologías Principales

- **Java 11 + Maven** → Desarrollo y gestión de dependencias  
- **JUnit 5** → Ejecución y organización de tests  
- **Selenium WebDriver** → Automatización de navegadores  
- **ExtentReports** → Generación de reportes gráficos  

---

## 🏗️ Patrones de Diseño Implementados

- **Page Object Model (POM)**  
  Separa la interacción con la UI de la lógica de pruebas.

- **Singleton**  
  Garantiza una única instancia de WebDriver.

- **Factory**  
  Permite la creación de drivers para distintos navegadores.

- **Fachada (Facade)**  
  Simplifica y orquesta flujos complejos de prueba.

---

## ⚙️ Características Clave

- ✅ Ejecución **Cross-Browser** (Chrome y Edge)  
- ✅ **Parametrización** mediante archivos `.properties`  
- ✅ Organización de tests mediante **@Tag ("regresion")**  
- ✅ **Reportes automáticos HTML** con métricas de ejecución  

---

## 🧩 Arquitectura del Framework
Tests JUnit → Fachada → Page Objects → Selenium → Navegadores

---

## ▶️ Comandos de Ejecución

```bash
# Suite completa
mvn test

# Tests por tag "regresion"
mvn test -Dgroups="regresion"

# Suite por clase
mvn test -Dtest=SuitePorClase

# Suite por paquete
mvn test -Dtest=SuitePorPaquete

# Suite por tags
mvn test -Dtest=SuitePorTags

# Test específico
mvn test -Dtest="Test01_CrearAdmin"

🧪 Cobertura de Funcionalidades

El framework cubre funcionalidades críticas del sistema:

🔐 Gestión de Usuarios Administradores
Creación de cuentas admin
Autenticación
👥 Ciclo de Vida de Testers
Creación de testers
Visualización en listas
Eliminación de perfiles
🔑 Administración de Credenciales
Reinicio de contraseñas
Validación de autenticación

📋 Escenarios de Prueba
Test	Escenario	Validaciones
Test01_CrearAdmin	Creación de usuario admin	✔ Creación exitosa
✔ Login válido
Test02_CrearTester	Registro de tester	✔ Creación
✔ Presencia en lista
Test03_BorrarCuentaTester	Eliminación de tester	✔ Eliminación
✔ Desaparición en lista
Test04_ReiniciarPass	Recuperación de credenciales	✔ Reset exitoso
✔ Login con nueva password

🔎 Cada test valida:

Flujo positivo
Persistencia de datos
Integridad del sistema post-operación
