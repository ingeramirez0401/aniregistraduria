---
title: Arquitectura de la Aplicación - Atributos de Calidad
has_children: false
more-content: true
ordered: true
parent: ANI Registraduria 
toc: true
---

# Atributos de Calidad.

[Regresar al principal](../../plantilla-arquitectura-aplicacion.html)

<!-- No importa como se llame a un atributo de calidad, siempre y cuando un escenario describa que significa. Se identificaron escenarios principalmente de los siguientes tipos:  caso de uso, de crecimiento y exploratorios. Se debe asegurar que exista algún escenario que represente cada driver arquitectónico.
Describa cada uno de los escenarios (lo conforman los atributos de calidad), consolide los escenarios similares y logre consenso en los escenarios más importantes. Adicionalmente, se describen en mayor detalle el escenario teniendo en cuenta la estructura del punto 3.3. Finalmente, describir como los objetivos del negocio son alcanzados por el escenario --> 

**Atributo  de Calidad: Seguridad.**

| Escenario              | Autenticar en el sistema  |
| ---------------------- | ------------------------------------------------------------ |
| Origen                 | Usuario |
| Estimulo               | Autenticarse al servicio de ANI Registraduría |
| Artefacto Estimulado   | Componente de Autenticación |
| Ambiente               | Productivo |
| Respuesta              | Acceso concedido al sistema |
| Medida de la respuesta | Se concede acceso al sistema el 99% de las veces, según la configuración que se tenga para este usuario |

| Escenario              | Renovar el usuario de consulta de la API periódicamente |
| ---------------------- | ------------------------------------------------------------ |
| Origen                 | Sistema |
| Estimulo               | Validación del usuario de consulta |
| Artefacto Estimulado   | Componente de Validación de servicio de Registraduría |
| Ambiente               | Productivo |
| Respuesta              | Cambio de contraseña del usuario de consulta |
| Medida de la respuesta | El sistema debe solicitar cambio de contraseña del usuario de consulta de Registraduría cada 6 meses. |

**Atributo  de Calidad: Disponibilidad.**

| Escenario              | Acceso y gestión de las solicitudes   |
| ---------------------- | ------------------------------------------------------------ |
| Origen                 | Usuario |
| Estimulo               | Sistema Completo  |
| Artefacto Estimulado   | Sistema Completo  |
| Ambiente               | Productivo |
| Respuesta              | Acceso y gestión de las solicitudes  |
| Medida de la respuesta | Se debe poder gestionar el 100% de las solicitudes |

**Atributo  de Calidad: Testeabilidad.**

| Escenario              | Validar la gestión de consultas de cédulas de ciudadanía |
| ---------------------- | ------------------------------------------------------------ |
| Origen                 | Aplicación |
| Estimulo               | Ejecución de pruebas unitarias |
| Artefacto Estimulado   | Código fuente compilado |
| Ambiente               | Productivo |
| Respuesta              | Resultado de los casos de pruebas unitarias |
| Medida de la respuesta | La cobertura debe ser mayor o igual al 70% |

**Atributo  de Calidad: Mantenibilidad.**

| Escenario              | Gestionar el estado de salud del servicio en muy poco tiempo |
| ---------------------- | ------------------------------------------------------------ |
| Origen                 | Aplicación |
| Estimulo               | Ejecución de pruebas y análisis de funcionalidad |
| Artefacto Estimulado   | Toda la Plataforma |
| Ambiente               | Productivo |
| Respuesta              | Restablecimiento del servicio inmediato a la gestión de salud |
| Medida de la respuesta | El tiempo de restablecimiento de la plataforma debido a gestiones de mantenimiento, salud o funcionalidad no debe superar 1 hora como máximo |

**Atributo  de Calidad: Adaptabilidad.**

| Escenario              | El servicio se debe poder consultar desde cualquier aplicación de EPM |
| ---------------------- | ------------------------------------------------------------ |
| Origen                 | Usuario |
| Estimulo               | Sistema completo |
| Artefacto Estimulado   | Toda la Plataforma |
| Ambiente               | Productivo |
| Respuesta              | La plataforma es accedida desde el dominio de EPM |
| Medida de la respuesta | La plataforma debe poderse acceder a través de una integración API desde cualquier aplicación de EPM que cumpla los requisitos mínimos de integración |
