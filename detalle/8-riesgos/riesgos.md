---
title: Arquitectura de la Aplicación - Riesgos
has_children: false
more-content: true
ordered: true
parent: ANI Registraduria 
toc: true
---

# Riesgos.

[Regresar al principal](../../plantilla-arquitectura-aplicacion.html)

Enumere cada uno de los riesgos o también los puntos de interés que deben ser vigilados frecuentemente para evitar posibles malos funcionamientos de la solución.

Apóyese en las desventajas y puntos de interés de las arquitecturas de referencia consultadas para diseñar esta solución.


| Objeto  afectado        | Tipo del riesgo            | Descripción e impacto del riesgo                             |
| ----------------------- | -------------------------- | ------------------------------------------------------------ |
|Integración con Registraduría|Indisponibilidad|Se pueden presentar intermitencias del servicio debido a mantenimientos programados o no, fallos o novedades presentados en el proveedor o caída completa del sistema. Todos estos factores son ajenos a la aplicación tratándose de una integración externa.|
|Infraestructura|Indisponibilidad del Servicio|Al tratarse de una aplicación relativamente pequeña se plantea una solución de tipo API que, de presentarse alguna necesidad de mantenimiento o novedad presentada se podrían presentar intermitencias o se detenga el servicio completamente por el tiempo necesario antes de poner nuevamente en funcionamiento. De igual forma un mantenimiento programado o corrección en el servidor pueden generar intermitencias que se traduce en que las aplicaciones que consumen el servicio pueden presentar novedades.|
