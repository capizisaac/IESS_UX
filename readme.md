# 🏛️ Rediseño y Optimización UX - Portal de Consultas del IESS

Repositorio oficial del prototipo funcional de la fase de investigación, auditoría y desarrollo de experiencia de usuario (UX) para el portal de consultas del Instituto Ecuatoriano de Seguridad Social (**IESS**).

---

## 📋 Descripción General del Proyecto
El objetivo principal de este proyecto es rediseñar y optimizar la experiencia de usuario en el flujo de consulta de solicitudes y certificados del portal web del IESS (`www.iess.gob.ec`), mitigando los altos niveles de fricción, la obsolescencia visual y los bloqueos técnicos experimentados por los ciudadanos y gestores en la plataforma actual.

---

## 👥 1. Investigación de Usuarios y Personas (UX Research)
A partir de un estudio cualitativo con 7 perfiles diversos, se sintetizaron **3 arquetipos clave** que representan el espectro real de usuarios del sistema:

*   **Persona 1: Alejandro Ramos (23 años) - El Joven Independiente / Principiante**
    *   *Perfil:* Desarrollador Junior con alta afinidad tecnológica pero totalmente desorientado frente a la burocracia y la terminología legal del IESS.
    *   *Necesidades:* Acceso móvil rápido, lenguaje claro ("en cristiano") y guías simplificadas.
*   **Persona 2: Carlos Vaca (68 años) - El Adulto Mayor / Jubilado**
    *   *Perfil:* Contador jubilado con baja afinidad digital y alta aversión al riesgo (miedo a perder sus trámites de jubilación).
    *   *Necesidades:* Tipografías legibles, alto contraste, menús sin ambigüedades y navegación asistida paso a paso.
*   **Persona 3: Elena Mora (32 años) - La Gestora / Operadora de Ciber**
    *   *Perfil:* Administradora de un cibernegocio que utiliza el portal a diario para atender a múltiples clientes.
    *   *Necesidades:* Estabilidad del sistema, persistencia de sesión ampliada, atajos eficientes y procesamiento por lotes para evitar tiempos muertos.

---

## 🔍 2. Auditoría Heurística (Basada en los 10 Principios de Jakob Nielsen)
Se evaluó el portal actual cruzando los problemas reales identificados con los estándares de usabilidad de Nielsen, aplicando las siguientes correcciones arquitectónicas:

1.  **Visibilidad del estado del sistema:** Implementación de *spinners* asíncronos y contenedores de carga en segundo plano para evitar la percepción de congelamiento.
2.  **Relación entre el sistema y el mundo real:** Supresión de jergas técnicas excesivas en favor de descripciones accesibles.
3.  **Control y libertad del usuario:** Rutas de navegación fluidas que evitan la invalidación abrupta de sesión mediante el uso del historial.
4.  **Consistencia y estándares:** Unificación de un sistema de diseño (*Design System*) homogéneo frente a la mezcla de interfaces heredadas.
5.  **Prevención de errores:** Análisis previo de datos en caché/sesión y validación estricta de campos en tiempo real antes de enviar peticiones.
6.  **Reconocimiento antes que recuerdo:** Uso de almacenamiento local (*LocalStorage*) para recordar datos recurrentes de identidad (cédulas consultadas).
7.  **Flexibilidad y eficiencia de uso:** Optimización del flujo para reducir el número de clics innecesarios en consultas repetitivas.
8.  **Diseño estético y minimalista:** Eliminación de banners de ruido visual institucional para priorizar el espacio de trabajo.
9.  **Ayuda en la recuperación de errores:** Traducción de códigos crípticos de servidor a mensajes humanos constructivos.
10. **Ayuda y documentación contextual:** Incorporación de tooltips informativos en los puntos críticos de consulta.

---

## 🗺️ 3. User Journeys (Mapeo de Recorridos)
El rediseño optimizó los puntos críticos detectados en los recorridos de los usuarios:
*   **Fase de Acceso:** Solución de problemas de diseño no responsivo (*Mobile-First* aplicado).
*   **Fase de Búsqueda:** Reducción de menús anidados confusos.
*   **Fase de Ejecución:** Persistencia local de datos y feedback inmediato mediante indicadores de carga asíncrona.

---

## 💻 4. Especificaciones Técnicas del Prototipo Web
El prototipo funcional alojado en este repositorio cumple con los siguientes lineamientos de desarrollo frontend:
*   **Estructura Modular:** Código limpio dividido estrictamente en `index.html` (marcado semántico) y `styles.css` (diseño responsivo con variables CSS y paleta inspirada en estándares institucionales modernos).
*   **Arquitectura Frontend:** 
    *   Uso de `localStorage` para persistencia de datos de usuario.
    *   Simulación de llamadas asíncronas seguras con manejo de estados intermedios.
    *   Validaciones nativas en formularios para prevenir envíos erróneos.

---

## 📂 Estructura del Repositorio
```text
IESS_UX/
│
├── index.html       # Interfaz principal optimizada (Mobile-first, validaciones y estados)
└── styles.css       # Hoja de estilos modular, moderna y responsiva