# Briefing de GymFlow

## 1. Qué es GymFlow
GymFlow es un sistema para gestionar un gimnasio con clases dirigidas. Tiene dos aplicaciones que comparten los mismos datos:

- **GymFlow Socio:** app móvil para que los socios consulten el horario y reserven clases.
- **GymFlow Recepción:** aplicación de escritorio para que el personal gestione socios, clases y reservas.

## 2. Objetivos

### Objetivo principal
Que un socio pueda reservar una clase desde el móvil en pocos pasos y que la recepción pueda gestionarlo todo de forma rápida y sin errores.

### Objetivos por aplicación
| Aplicación | Tipo de aplicación | Qué prioriza el diseño |
|---|---|---|
| Socio | Transaccional | Completar la reserva en el mínimo de pasos |
| Recepción | Herramienta de gestión | Eficiencia: hacer las tareas del día a día rápidamente |

### Objetivos medibles (usabilidad, ISO 9241-11)
- **Eficacia:** el socio completa una reserva sin ayuda.
- **Eficiencia:** reservar una clase en 3 toques o menos desde el inicio.
- **Tolerancia al error:** no se puede reservar una clase llena; la app ofrece la lista de espera.
- **Satisfacción:** el usuario encuentra la app clara y agradable.

## 3. Usuarios

| Grupo | Funcionalidades | Experiencia | Dispositivo | Contexto de uso |
|---|---|---|---|---|
| Socio | Usuario registrado | De novato a experto | Móvil | Fuera del gimnasio (casa, transporte) o en la entrada |
| Recepcionista | Administrador | De intermedio a experto | Ordenador | Mostrador de recepción, a menudo con gente esperando |

- Los socios tienen edades, conocimientos informáticos y capacidades muy distintos; la app tiene que ser fácil para todos, incluidas las personas con necesidades de accesibilidad.
- Las dos personas que representan a los socios están en el documento [03-personas.md](03-personas.md).
- Datos obtenidos en la entrevista: ver [02-entrevista.md](02-entrevista.md).

## 4. Contenidos y funcionalidades

### GymFlow Socio (móvil)
- Inicio con la próxima clase reservada
- Horario de clases (día, hora, monitor, sala, plazas libres)
- Reservar y anular una clase
- Lista de espera cuando la clase está llena
- Mis reservas
- Perfil del socio
- Ayuda

### GymFlow Recepción (escritorio)
- Panel del día (clases y ocupación)
- Gestión de socios (alta, búsqueda, edición, baja)
- Gestión de clases y horarios
- Gestión de reservas y lista de espera
- Control de asistencia

## 5. Requisitos

### Requisitos de diseño y usabilidad
- **Mobile first** para la app de Socio: se diseña primero en formato vertical y de una sola columna.
- Principios de Nielsen prioritarios: **1. Visibilidad del estado del sistema**, **4. Consistencia y estándares** y **5. Prevención de errores**.
- Mensajes con palabras del usuario («Clase llena», no «Error 409»).
- Recepción: atajos de teclado para los usuarios expertos.

### Requisitos de accesibilidad
- Cumplimiento de las **WCAG 2.2 nivel AA**.
- Contraste de color suficiente e información que no dependa solo del color.
- Texto alternativo en los iconos y compatibilidad con lectores de pantalla (TalkBack, VoiceOver).
- Tamaño mínimo de los botones y uso cómodo con una sola mano.
- Recepción utilizable solo con el teclado.

### Requisitos técnicos
- **Dos front-ends:** una app móvil (Socio) y una aplicación de escritorio (Recepción).
- **Un back-end compartido:** servidor y base de datos comunes, para que una reserva hecha desde el móvil se vea al momento en recepción.
- Se necesita conexión a Internet para reservar; la app debe avisar claramente si no la hay.
- **Herramientas de diseño:** Figma / FigJam para mapas, wireframes y prototipos.

## 6. Competencia

| App | Qué hace bien | Qué evitaremos |
|---|---|---|
| Basic-Fit | Gráfico de afluencia del club y botón de acceso siempre visible | Errores sin explicación e iconos sin etiqueta |

El análisis completo de Basic-Fit está en el documento [01-analisi-nielsen.md](01-analisi-nielsen.md).

## 7. Planificación

| Semanas | Fase | Entregables |
|---|---|---|
| 9 | Planificación | Briefing, entrevista, personas, mapas de navegación y bocetos |
| 10 | Diseño | Wireframes |
| 11 | Diseño | Mockups y prototipo navegable |
| 12-27 | Desarrollo y pruebas | Aplicaciones Socio y Recepción |
| 29-30 | Distribución | Publicación de las aplicaciones |
