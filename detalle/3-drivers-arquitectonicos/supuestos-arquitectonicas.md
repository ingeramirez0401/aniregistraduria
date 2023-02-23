---
title: Arquitectura de la Aplicación - Supuestos Arquitectónicas
has_children: false
more-content: true
ordered: true
parent: ANI Registraduria 
toc: true
---

# Supuestos Arquitectónicas.

[Regresar al principal](../../plantilla-arquitectura-aplicacion.html)

A continuación, describimos los supuestos que complementan la descripción de los drivers arquitectónicos del sistema:

- Se asume que para dar cumplimiento al atributo de calidad de seguridad se deben implementar los lineamientos de seguridad exigidos por Registraduría para la integración con el servicio expuesto por ellos; de igual forma, este servicio debe garantizar la actualización de la clave de acceso del usuario de consulta cada 6 meses como mínimo.

 - Se debe dar cumplimiento con los lineamientos mínimos requeridos de arquitecturas modernas definidas entre IG y EPM para garantizar la disponibilidad y el acceso a los recursos entre Registraduría y EPM y con ellos garantizar un optimo servicio de consulta de cédulas de ciudadanía.

- Se deban utilizar las practicas DevOps establecidas entre IG y EPM tales como Monitoreo Continuo, Despliegue Continuo, Pruebas Unitarias, Pruebas de Seguridad, Integración Continua, Gestión de Errores, Gestión de Tareas, Control de Código, Control de documentación que garanticen la correcta ejecución de todos los servicios y la gestión de los recursos.

- Para dar cumplimiento al atributo de disponibilidad se debe garantizar el servicio las 24 horas al día, los 7 días a la semana y que los tiempos de interrupción que se presenten, sean mínimos y se garantice una estabilización pronta del servicio.

- Se debe garantizar el acceso al servicio de consultas de cédulas a usuarios del dominio activo de EPM, también se debe garantizar un servicio API de fácil integración para que sea utilizado por cualquier aplicación que requiera prestar este servicio de consulta dentro de sus operaciones de negocio.