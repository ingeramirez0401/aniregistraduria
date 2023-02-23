---
title: Arquitectura de la Aplicación - Restricciones Funcionales
has_children: false
more-content: true
ordered: true
parent: ANI Registraduria 
toc: true
---

# Restricciones Funcionales.

[Regresar al principal](../../plantilla-arquitectura-aplicacion.html)

Enumere en orden de importancia las restricciones funcionales que se presentan en la solución

- Tiempos de respuesta: Los tiempos de consulta y de respuesta al BackEnd deben ser bajos.
  Nota: Se debe garantizar este tiempo internamente, el sistema no puede ni podrá controlar los tiempos de respuesta de la integración al tratarse de un sistema externo.

- Azure Active Directory: Las consultas a realizar desde la plataforma se debe hacer internamente mediante usuarios del directorio activo de EPM.

- Notificaciones: La notificación por correo se debe consumir por el servicio expuesto en Azure.

- Estándar de integración: La Registraduría Nacional del Estado Civil proporciona acceso a los web services por medio de un contrato inter administrativo con EPM y las consultas se deben hacer mediante llaves de encriptado y desencriptado.

- Cifrado de la información: Toda la información que viaje por medio del API debe ser encriptado durante el viaje de la información. Por medio de un par de llaves públicas y privadas se podrá desencriptar y encriptar la información.

- Consulta de información: La aplicación debe ser capaz de consultar las cédulas de identidad a través de la integración con el servicio de Registraduría de forma independiente o masiva.

- Identificar riesgos potenciales que pueden afectar la implementación del sistema.

- Identificar conceptos del sistema que son relevantes a la arquitectura.

- Definir y delimitar el sistema mediante la definición de la arquitectura técnica y funcional.

- Definir y establecer directrices para arquitectura con enfoques modernos.

- Definir y establecer directrices para diseño e implementación del sistema.

- Identificar el uso de comportamientos comunes con el fin de que las implementaciones se hagan por medio de patrones y reutilización.

- Fomentar el uso de Clean Code y buenas prácticas en la implementación de las funcionalidades.

- Implementar Practicas DevOps.