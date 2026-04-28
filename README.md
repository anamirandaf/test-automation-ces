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

## 🧪 Cobertura de Funcionalidades

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

## 📋 Escenarios de Prueba
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

## 🧪 Suites Ejecutadas
Suite por Clases
Suite por Paquetes
Suite por Tags

## 🌐 Datos del Ambiente
Sistema Bajo Prueba
URL: http://cestore.ces.com.uy/adminces/
Versión: v1.1.0
Usuarios:
Admin: admin@gmail.com
Tester: test@gmail.com
Fecha del sistema: 29/08/2025

## 💻 Entorno de Ejecución
Sistema Operativo: Windows
Navegadores: Chrome, Edge
IDE: IntelliJ IDEA Community Edition 2025.1
Selenium: 4.18.1

Drivers:

ChromeDriver v140.0.7339.207
Edge WebDriver (Stable)

## 📈 Reportes

Los reportes se generan automáticamente en formato HTML mediante ExtentReports, incluyendo:

Resultados por test
Métricas de ejecución
Evidencias (si aplica)

## 📌 Conclusión

Este framework proporciona una solución robusta, mantenible y escalable para asegurar la calidad del sistema mediante automatización de pruebas.

Permite:

Ejecución flexible
Fácil mantenimiento
Alta reutilización de código
