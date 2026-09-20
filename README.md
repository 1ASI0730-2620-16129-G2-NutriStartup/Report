# NutriApp Integral

## 4.5. Web Applications Prototyping

### Introducción y criterios de diseño

El prototipo interactivo de **NutriApp Integral** representa la navegación y los principales flujos de la plataforma web. Su finalidad es validar la organización de las funciones, la facilidad de uso y la experiencia de los usuarios antes de comenzar el desarrollo del producto.

El prototipo considera los dos segmentos objetivos identificados durante la investigación: personas que desean reducir o controlar su peso y nutricionistas interesados en brindar consultas digitales, realizar seguimiento a sus pacientes y generar ingresos adicionales.

**Orientación según el tipo de usuario:** La interfaz presenta funciones diferentes según el rol seleccionado. Los pacientes pueden registrar sus avances, consultar su plan alimenticio, recibir recomendaciones y reservar citas. Por otro lado, los nutricionistas pueden gestionar pacientes, elaborar planes personalizados, revisar indicadores de progreso y administrar sus consultas.

**Consistencia en los patrones de interacción:** La plataforma mantiene una estructura visual uniforme en sus diferentes módulos. Se utiliza un menú lateral para acceder a las funciones principales, formularios para registrar información, ventanas modales para confirmar acciones importantes y notificaciones para comunicar resultados o recordar actividades pendientes.

**Personalización de la experiencia:** La información mostrada se adapta al perfil, objetivos y progreso de cada usuario. Los planes alimenticios y recomendaciones consideran datos como peso, talla, preferencias alimentarias, presupuesto, disponibilidad de tiempo y meta nutricional.

**Prevención de errores:** Las acciones que pueden modificar información importante, como eliminar un registro, cancelar una cita o cambiar un plan alimenticio, solicitan confirmación antes de ejecutarse. Los formularios también incluyen validaciones para evitar datos incompletos o valores incorrectos.

**Retroalimentación inmediata:** Después de registrar el peso, completar una actividad, reservar una consulta o actualizar un plan nutricional, la plataforma muestra un mensaje de confirmación. Los gráficos de progreso también se actualizan con la nueva información registrada.

**Accesibilidad y diseño responsive:** Los elementos interactivos presentan un tamaño adecuado, textos legibles y suficiente contraste. El prototipo está diseñado para adaptarse a computadoras, tablets y teléfonos móviles, debido a que los entrevistados señalaron que utilizarían principalmente el celular.

**Uso responsable de la inteligencia artificial:** Las recomendaciones generadas mediante inteligencia artificial funcionan como una herramienta de apoyo. Estas no reemplazan el diagnóstico, la evaluación ni el criterio profesional del nutricionista.

> **PENDIENTE: Imagen del prototipo general de NutriApp Integral.**  
> **Motivo:** Primero deben diseñarse y conectar en Figma las pantallas definitivas de ambos roles.  
> **Imagen requerida:** Vista general de todos los frames del prototipo, incluyendo las pantallas del paciente y del nutricionista.

### Flujos de interacción cubiertos por el prototipo

El prototipo de **NutriApp Integral** debe representar los siguientes flujos principales:

#### Flujo 1 — Registro y configuración del perfil nutricional

El usuario crea una cuenta, inicia sesión y completa su perfil con información como edad, peso, talla, objetivo, preferencias alimentarias, restricciones, disponibilidad de tiempo y presupuesto. Después de validar los datos, la plataforma crea su perfil nutricional y muestra el panel principal.

> **PENDIENTE: Imagen del flujo de registro y configuración del perfil.**  
> **Motivo:** Se requieren las pantallas conectadas en Figma para representar correctamente la navegación.  
> **Imagen requerida:** Creación de cuenta → inicio de sesión → registro de datos personales → selección de objetivo → registro de preferencias → confirmación del perfil → panel principal.

#### Flujo 2 — Generación y consulta del plan nutricional

El usuario solicita un plan alimenticio de acuerdo con su perfil y objetivo. El sistema procesa la información registrada y propone un plan semanal personalizado. El usuario puede revisar las comidas recomendadas, reemplazar opciones disponibles y solicitar la evaluación de un nutricionista.

> **PENDIENTE: Imagen del flujo de generación del plan nutricional.**  
> **Motivo:** Todavía debe elaborarse el prototipo visual de las recomendaciones y del plan semanal.  
> **Imagen requerida:** Panel principal → solicitud de plan → configuración de preferencias → plan generado → detalle de comidas → solicitud de revisión profesional.

#### Flujo 3 — Registro y visualización del progreso

El usuario registra periódicamente su peso, medidas corporales, alimentación y actividad física. La plataforma procesa los datos y presenta gráficos que permiten comparar los resultados con la meta establecida.

> **PENDIENTE: Imagen del flujo de seguimiento del progreso.**  
> **Motivo:** Se necesitan las pantallas finales de registro de avances y visualización de estadísticas.  
> **Imagen requerida:** Panel principal → registrar progreso → ingresar peso y medidas → guardar registro → visualizar gráficos e indicadores.

#### Flujo 4 — Reserva y atención de una consulta nutricional

El usuario revisa los perfiles de los nutricionistas disponibles, selecciona uno y consulta sus horarios. Luego reserva una cita y recibe una confirmación. El nutricionista puede revisar la solicitud, acceder a la información autorizada del paciente y realizar el seguimiento correspondiente.

> **PENDIENTE: Imagen del flujo de reserva de consulta.**  
> **Motivo:** Todavía deben conectarse las pantallas correspondientes al paciente y al nutricionista.  
> **Imagen requerida:** Lista de nutricionistas → perfil profesional → horarios disponibles → confirmación de reserva → agenda del nutricionista → atención o seguimiento.

#### Flujo 5 — Gestión y seguimiento de pacientes

El nutricionista visualiza a sus pacientes, consulta sus registros, revisa su evolución y crea o modifica sus planes nutricionales. También puede enviar recomendaciones y recordatorios para mejorar la constancia del paciente.

> **PENDIENTE: Imagen del flujo de gestión de pacientes.**  
> **Motivo:** Se requiere diseñar el panel profesional y sus módulos de seguimiento.  
> **Imagen requerida:** Panel del nutricionista → lista de pacientes → perfil del paciente → historial de progreso → creación o actualización del plan → envío de recomendación.

## 4.6. Domain-Driven Software Architecture

La arquitectura de **NutriApp Integral** se diseña siguiendo los principios de **Domain-Driven Design (DDD)**. Este enfoque permite organizar el sistema según los procesos y reglas principales del negocio, estableciendo límites claros entre las funcionalidades destinadas a los pacientes y aquellas utilizadas por los nutricionistas.

A partir del análisis de las entrevistas, las necesidades de los usuarios y las funcionalidades planteadas, se identificaron los siguientes dominios:

1. **Identity and Access Management:** gestiona el registro, autenticación, recuperación de contraseña y permisos según el rol del usuario.
2. **User Profile Management:** administra los datos personales, objetivos, preferencias y restricciones del paciente, además de la información profesional del nutricionista.
3. **Nutrition Plan Management:** permite crear, generar, revisar y actualizar planes nutricionales personalizados.
4. **Progress Monitoring:** gestiona el registro y la visualización del peso, medidas corporales, alimentación, actividad física y cumplimiento de objetivos.
5. **Appointment Management:** administra la disponibilidad de los nutricionistas, la reserva de consultas y el seguimiento posterior de los pacientes.

Esta separación facilita la evolución independiente de cada dominio, reduce el acoplamiento entre los componentes y mantiene un lenguaje común entre los integrantes del equipo.

### 4.6.1. Design-Level EventStorming

El Design-Level EventStorming de **NutriApp Integral** permite representar los comandos, eventos, actores, reglas y conceptos que participan en sus principales procesos. Mediante este análisis se identifican las responsabilidades de cada dominio y la comunicación necesaria entre ellos.

#### 1. Identity and Access Management

**Gestión de identidad y acceso**

**Propósito:** Gestionar el registro, autenticación, recuperación de contraseña, sesiones y permisos de los pacientes, nutricionistas y administradores.

**Clasificación estratégica:** Dominio genérico de autenticación y seguridad.

**Roles del dominio:** Paciente, nutricionista, administrador y servicio de autenticación.

**Comunicación entrante:**

- Solicitud de registro de usuario.
- Comando autenticar usuario.
- Comando cerrar sesión.
- Solicitud restablecer contraseña.
- Comando asignar rol.

**Comunicación saliente:**

- Evento usuario registrado.
- Evento usuario autenticado.
- Evento sesión cerrada.
- Evento contraseña restablecida.
- Evento rol asignado.

**Lenguaje ubicuo:** Cuenta de usuario, credenciales, sesión, rol, permiso, token de autenticación y estado de cuenta.

**Decisiones de negocio:**

- Cada correo electrónico solo puede estar asociado con una cuenta.
- El acceso a las funciones depende del rol asignado.
- Las contraseñas deben cumplir los requisitos mínimos de seguridad.
- Los nutricionistas deben completar la información profesional requerida.

**Supuestos:** Los usuarios cuentan con un correo electrónico válido y acceso a internet para registrarse y autenticarse.

**Métricas de verificación:** Porcentaje de registros completados, porcentaje de accesos exitosos, tiempo promedio de autenticación, intentos fallidos y solicitudes de recuperación de contraseña.

**Preguntas abiertas:**

- ¿Se verificará obligatoriamente el correo electrónico?
- ¿Se utilizará autenticación mediante Google?
- ¿Cómo se validarán las credenciales profesionales de los nutricionistas?

> **PENDIENTE: Imagen del EventStorming de Identity and Access Management.**  
> **Motivo:** La información anterior debe organizarse visualmente en Miro, FigJam o Figma.  
> **Imagen requerida:** Propósito, clasificación, roles, comunicación entrante y saliente, lenguaje ubicuo, decisiones, supuestos, métricas y preguntas abiertas.

#### 2. User Profile Management

**Gestión de perfiles de usuario**

**Propósito:** Gestionar los datos personales, objetivos, preferencias y restricciones de los pacientes, así como la información profesional y disponibilidad de los nutricionistas.

**Clasificación estratégica:** Dominio de soporte.

**Roles del dominio:** Paciente, nutricionista, administrador y gestor de perfiles.

**Comunicación entrante:**

- Comando crear perfil.
- Comando actualizar información personal.
- Comando registrar objetivo nutricional.
- Comando registrar preferencias alimentarias.
- Comando registrar restricción alimentaria.
- Comando actualizar perfil profesional.

**Comunicación saliente:**

- Evento perfil creado.
- Evento información personal actualizada.
- Evento objetivo nutricional registrado.
- Evento preferencias actualizadas.
- Evento restricción registrada.
- Evento perfil profesional actualizado.

**Lenguaje ubicuo:** Perfil de paciente, perfil profesional, objetivo nutricional, preferencia alimentaria, restricción alimentaria, presupuesto, disponibilidad y datos antropométricos.

**Decisiones de negocio:**

- El paciente debe completar los datos mínimos antes de solicitar un plan.
- Las restricciones alimentarias deben considerarse en todas las recomendaciones.
- El perfil del nutricionista debe mostrar su especialidad y experiencia.
- Los datos sensibles solo pueden consultarse con autorización.

**Supuestos:** Los usuarios proporcionan información verdadera y actualizan sus datos cuando se produce algún cambio relevante.

**Métricas de verificación:** Porcentaje de perfiles completados, tiempo promedio para completar el perfil, perfiles actualizados y porcentaje de nutricionistas con información verificada.

**Preguntas abiertas:**

- ¿Qué datos serán obligatorios para crear un perfil?
- ¿Los pacientes podrán ocultar determinados datos?
- ¿Cada cuánto tiempo se solicitará actualizar el peso y las medidas?

> **PENDIENTE: Imagen del EventStorming de User Profile Management.**  
> **Motivo:** Debe construirse la representación visual del dominio a partir de los elementos definidos.  
> **Imagen requerida:** Comandos, eventos, conceptos y decisiones relacionados con los perfiles de pacientes y nutricionistas.

#### 3. Nutrition Plan Management

**Gestión de planes nutricionales**

**Propósito:** Crear, generar, revisar y actualizar planes alimenticios personalizados según los objetivos, preferencias y restricciones del paciente.

**Clasificación estratégica:** Dominio núcleo.

**Roles del dominio:** Paciente, nutricionista, asistente de recomendaciones y gestor de planes nutricionales.

**Comunicación entrante:**

- Comando solicitar plan nutricional.
- Comando generar propuesta de plan.
- Comando crear plan personalizado.
- Comando modificar plan.
- Comando aprobar plan.
- Comando reemplazar alimento.

**Comunicación saliente:**

- Evento plan solicitado.
- Evento propuesta generada.
- Evento plan nutricional creado.
- Evento plan actualizado.
- Evento plan aprobado.
- Evento alimento reemplazado.

**Lenguaje ubicuo:** Plan nutricional, plan semanal, comida, alimento, porción, restricción alimentaria, preferencia, objetivo nutricional, recomendación y sustitución de alimento.

**Decisiones de negocio:**

- Ningún plan puede incluir alimentos registrados como restringidos.
- Las recomendaciones deben considerar el objetivo y las preferencias del paciente.
- Los planes creados por inteligencia artificial son propuestas sujetas a revisión.
- El nutricionista conserva la decisión final sobre el tratamiento nutricional.
- Los cambios realizados en un plan deben conservarse en el historial.

**Supuestos:** El paciente ha completado previamente su perfil nutricional y sus datos se encuentran actualizados.

**Métricas de verificación:** Cantidad de planes generados, porcentaje de planes revisados, modificaciones por plan, cumplimiento semanal y satisfacción con las recomendaciones.

**Preguntas abiertas:**

- ¿Qué modelo de inteligencia artificial se utilizará?
- ¿Qué información nutricional será necesaria para generar los planes?
- ¿Cómo se advertirá al usuario que una recomendación no reemplaza una consulta profesional?

> **PENDIENTE: Imagen del EventStorming de Nutrition Plan Management.**  
> **Motivo:** Los comandos, eventos y reglas deben trasladarse a un tablero visual.  
> **Imagen requerida:** Proceso desde la solicitud del plan hasta su generación, revisión, aprobación y actualización.

#### 4. Progress Monitoring

**Monitoreo del progreso**

**Propósito:** Registrar y analizar la evolución del paciente mediante datos relacionados con su peso, medidas corporales, alimentación, actividad física y cumplimiento del plan.

**Clasificación estratégica:** Dominio núcleo.

**Roles del dominio:** Paciente, nutricionista, servicio de seguimiento y sistema de notificaciones.

**Comunicación entrante:**

- Comando registrar peso.
- Comando registrar medidas corporales.
- Comando registrar actividad física.
- Comando registrar cumplimiento del plan.
- Comando consultar progreso.
- Comando enviar recordatorio.

**Comunicación saliente:**

- Evento peso registrado.
- Evento medidas actualizadas.
- Evento actividad registrada.
- Evento cumplimiento actualizado.
- Evento progreso calculado.
- Evento recordatorio enviado.
- Evento meta alcanzada.

**Lenguaje ubicuo:** Registro de progreso, peso, medida corporal, actividad física, meta, indicador de progreso, cumplimiento, historial y recordatorio.

**Decisiones de negocio:**

- Los registros deben almacenarse con fecha y hora.
- Los datos históricos no deben reemplazarse al ingresar una nueva medición.
- Los gráficos deben mostrar la evolución respecto de la meta.
- Los recordatorios deben respetar la configuración del usuario.
- El nutricionista solo puede visualizar pacientes vinculados con su atención.

**Supuestos:** El usuario registra sus datos periódicamente y utiliza el mismo criterio de medición para mantener la consistencia del seguimiento.

**Métricas de verificación:** Frecuencia de registro de avances, usuarios activos semanalmente, cumplimiento promedio del plan, metas alcanzadas y tasa de abandono de registros.

**Preguntas abiertas:**

- ¿Con qué frecuencia se enviarán los recordatorios?
- ¿Se permitirá sincronizar datos con dispositivos inteligentes?
- ¿Qué indicadores serán visibles para el paciente y para el nutricionista?

> **PENDIENTE: Imagen del EventStorming de Progress Monitoring.**  
> **Motivo:** Falta elaborar el tablero visual correspondiente al seguimiento.  
> **Imagen requerida:** Registro de datos, cálculo del progreso, generación de gráficos, recordatorios y logro de metas.

#### 5. Appointment Management

**Gestión de citas y consultas nutricionales**

**Propósito:** Administrar la disponibilidad de los nutricionistas, la reserva de consultas, la comunicación con los pacientes y el seguimiento posterior a cada atención.

**Clasificación estratégica:** Dominio núcleo.

**Roles del dominio:** Paciente, nutricionista, administrador de agenda y servicio de notificaciones.

**Comunicación entrante:**

- Comando publicar disponibilidad.
- Comando consultar horarios.
- Comando reservar cita.
- Comando confirmar cita.
- Comando reprogramar cita.
- Comando cancelar cita.
- Comando registrar atención.

**Comunicación saliente:**

- Evento disponibilidad publicada.
- Evento cita reservada.
- Evento cita confirmada.
- Evento cita reprogramada.
- Evento cita cancelada.
- Evento consulta realizada.
- Evento seguimiento programado.

**Lenguaje ubicuo:** Agenda, disponibilidad, horario, cita, consulta virtual, estado de cita, reprogramación, cancelación, seguimiento y nutricionista asignado.

**Decisiones de negocio:**

- Una cita solo puede reservarse dentro de un horario disponible.
- El mismo horario no puede asignarse a dos pacientes.
- Las cancelaciones y reprogramaciones deben notificarse a ambas partes.
- El paciente debe autorizar el acceso del nutricionista a su información.
- Las consultas realizadas deben registrarse en el historial.

**Supuestos:** El nutricionista mantiene actualizada su disponibilidad y ambas partes cuentan con acceso a internet para realizar una consulta virtual.

**Métricas de verificación:** Número de citas reservadas, porcentaje de citas completadas, tasa de cancelaciones, tasa de reprogramaciones, tiempo entre la reserva y la atención e ingresos generados por consultas.

**Preguntas abiertas:**

- ¿La plataforma incorporará pagos en línea?
- ¿Qué política se aplicará ante cancelaciones tardías?
- ¿Se utilizará una videollamada interna o un servicio externo?
- ¿Cómo se calculará la comisión de la plataforma?

> **PENDIENTE: Imagen del EventStorming de Appointment Management.**  
> **Motivo:** Las reglas de reserva y atención deben representarse mediante un tablero visual.  
> **Imagen requerida:** Publicación de horarios, reserva, confirmación, reprogramación, cancelación, atención y seguimiento.

### Secciones pendientes para el final

- **4.6.2. Software Architecture Context Diagram**
- **4.6.3. Software Architecture Container Diagrams**
- **4.6.4. Software Architecture Components Diagrams**

Estas secciones se desarrollarán después de definir completamente la arquitectura técnica y revisar los ejemplos correspondientes.
